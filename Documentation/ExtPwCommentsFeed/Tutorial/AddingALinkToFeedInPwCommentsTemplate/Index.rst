.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. ==================================================
.. DEFINE SOME TEXTROLES
.. --------------------------------------------------
.. role::   underline
.. role::   typoscript(code)
.. role::   ts(typoscript)
   :class:  typoscript
.. role::   php(code)
.. highlight:: guess


Adding a link to feed in pw\_comments template
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

To add a text link to the feed, simply add this line: ::

   <f:translate extensionName="JhPwcommentsFeed" key="link.starting" /> <f:link.page absolute="1" pageType="{settings.feed_typenum}" target="_new"><f:translate extensionName="JhPwcommentsFeed" key="link.{settings.feed}" /></f:link.page>

to your pw\_comments fluid template in Comment/Index.html

If you want to overwrite the labels please use your template setup
like this: ::

   plugin.tx_jhpwcommentsfeed._LOCAL_LANG {
     default {
       link {
         starting = Guestbook as
         Rss091 =
         Rss2 =
         Atom1 =
       }
     }
   }