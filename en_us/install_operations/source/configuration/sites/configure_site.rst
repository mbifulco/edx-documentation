.. _Configuring Sites Independently:

#################################
Configuring Sites Independently
#################################

You can set configuration properties independently for individual sites. The
values you define for the individual sites override the default value that is
present in the ``cms.env.json`` or ``lms.env.json`` file. For example, you can
set the ``PLATFORM_NAME`` property to a different value for each of your sites
to indicate that the sites present courses for different organizations or
audiences.

*******************
Configuring a Site
*******************

To set configuration properties for a site, follow these steps.

#. Sign in to the Django administration console for your base URL. For example,
   ``http://{your_URL}/admin``.

#. Select **Site Configurations** to open the
   ``http://{hostname}/admin/site_configuration/siteconfiguration`` page.

#. Select **Add site configuration**.

#. From the **Site** menu, select the site you want to configure.

#. Enter configuration properties in the **Values** field. Structure all
   properties in valid JavaScript Object Notation (JSON) format.

   The following example shows a set of configuration properties for a site.

   .. code-block:: json

       {
         "course_email_from_addr":"courses@onlineu.edu",
         "university":"Online University",
         "PLATFORM_NAME":"Online University",
         "email_from_address":"courses@onlineu.edu",
         "payment_support_email":"payments@onlineu.edu",
         "SITE_NAME":"onlineu.edu",
         "site_domain":"onlineu.edu",
         "SESSION_COOKIE_DOMAIN":"onlineu.edu",
       }

#. When you are ready for the configuration settings to take effect,
   select **Enabled**.

   The configuration properties that you set do not affect the site
   until you select **Enabled**. If needed, you can return to the **Site
   configurations** screen for this site to enable the configuration properties
   later.

.. do you select Save or something else on this page? - Alison

*******************************
Site Configuration Reference
*******************************

You can define virtually any property in site configuration

{
  "ECOMMERCE_API_URL":"https://my-site.sandbox.edx.org/api/v2",
  "ECOMMERCE_PUBLIC_URL_ROOT":"https://my-site.sandbox.edx.org",
  "ECOMMERCE_API_SIGNING_KEY":"ecommerce-secret",
  "COURSE_CATALOG_VISIBILITY_PERMISSION":"see_in_catalog",
  "COURSE_ABOUT_VISIBILITY_PERMISSION":"see_about_page",
  "ENABLE_COMBINED_LOGIN_REGISTRATION":true,
  "ENABLE_PAID_COURSE_REGISTRATION":true,
  "ENABLE_SHOPPING_CART":true,
  "ENABLE_SHOPPING_CART_BULK_PURCHASE":false,
  "course_email_template_name":"my-site",
  "course_email_from_addr":"my-site@example.com",
  "ALLOW_AUTOMATED_SIGNUPS":true,
  "domain_prefix":"my-site",
  "university":"Education Programs",
  "PLATFORM_NAME":"Education Programs",
  "platform_name":"Education Programs",
  "show_only_org_on_student_dashboard":true,
  "email_from_address":"my-site@example.com",
  "payment_support_email":"payments@example.com",
  "ENABLE_EXTENDED_COURSE_DETAILS":true,
  "ENABLE_MKTG_SITE":false,
  "SITE_NAME":"my-site.sandbox.edx.org",
  "site_domain":"my-site.sandbox.edx.org",
  "SESSION_COOKIE_DOMAIN":"my-site.sandbox.edx.org",
  "ALWAYS_REDIRECT_HOMEPAGE_TO_DASHBOARD_FOR_AUTHENTICATED_USER":false,
  "ENABLE_COURSE_SORTING_BY_START_DATE":true,
  "ENABLE_THIRD_PARTY_AUTH":false,
  "course_org_filter":"MySiteX",
  "course_about_show_social_links":false,
  "show_partners":false,
  "show_homepage_promo_video":false,
  "homepage_promo_video_youtube_id":"<youtube-video-id>",
  "course_index_overlay_text":"<img src='/static/my-site/images/400x103.png' width='400' height='103' />",
  "homepage_overlay_html":"<img src='/static/my-site/images/400x103.png' width='400' height='103' />",
  "payment_email_signature":"Education Programs<br>The Digital Programs Team<br>my-site@example.com<br>101 Example Street<br>Example State",
  "student_profile_download_fields":[
    "id",
    "username",
    "name",
    "email",
    "language",
    "location",
    "year_of_birth",
    "gender",
    "level_of_education",
    "mailing_address",
    "goals",
    "meta.first-name",
    "meta.last-name",
    "meta.company",
    "meta.title",
    "meta.state",
    "meta.country"
  ],
  "REGISTRATION_EXTRA_FIELDS":{
    "first_name":"required",
    "last_name":"required",
    "level_of_education":"required",
    "gender":"required",
    "year_of_birth":"required",
    "mailing_address":"hidden",
    "goals":"hidden",
    "terms_of_service":"required",
    "honor_code":"required",
    "state":"required",
    "country":"required",
    "company":"required",
    "title":"required"
  },
  "extended_profile_fields":[
    "first_name",
    "last_name",
    "company",
    "title",
    "state",
    "country"
  ],
  "PDF_RECEIPT_COBRAND_LOGO_PATH":"/edx/app/edxapp/themes/edx-microsite/my-site/images/logo_pdf.gif",
  "PDF_RECEIPT_TERMS_AND_CONDITIONS":"CANCELLATIONS: Cancellation requests must be submitted to my-site@example.com 14 days prior to the course start date to be eligible for a refund. ...",
  "PDF_RECEIPT_BILLING_ADDRESS":"101 Example City Example State",
  "PDF_RECEIPT_LOGO_PATH":""
}

.. Saleem indicated that "Site configuration can be used to have site specific courses via ``course_org_filter`` setting" but in this example ( "course_org_filter":"MySiteX") is "MySiteX" the name of a course? I sould have expected a comma separated list of course IDs or some definition of what MySiteX means... - Alison
