.. _Configuring Sites Independently:

#################################
Configure Sites Independently
#################################

You can set configuration properties independently for individual sites. For
example, you can set the ``PLATFORM_NAME`` property toa different value for
each of your sites to indicate that the sites present courses for different
organizations or audiences.

.. What is the complete set of configuration properties that you can set for a
.. site? If you set a property for one or more sites, do you need to remove it
.. from lms.env.json? (question from Peter)

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

