What is this?
=============

This is the `Octopress classic theme`_, ported to be used with Nikola_.


How to install it?
==================

In your Nikola_ site:

#. Install the theme from the Nikola themes repository::

    $ nikola install_theme octopress

#. Edit your ``conf.py``, setting the variable ``THEME`` to ``octopress``::

     THEME = "octopress"

#. Rebuild your site::

     $ nikola build

That's it! You can also create the ``themes/`` directory yourself and manually clone this repository there (to the ``themes/octopress`` directory)


Configuration
=============

This theme has some improvements over typical Nikola_ themes, and they can be configured from the ``conf.py`` file.

To configure them, you can use the ``GLOBAL_CONTEXT`` variable.

Example
-------

This is an example; each variable is explained later. As you can see, I create a new variable for each section and then I add all of them to ``GLOBAL_CONTEXT``:

.. code:: python

    google_analytics = {
        'tracking_id': 'UA-9308241-1',
    }

    google_ads = {
      'pub': '1887364423515042',
      'slot': '7479875641',
      'width': 180,
      'height': 150,
    }

    github = {
      'username': 'magmax',
      'items': 3,
    }

    disqus = {
      'username': 'magmax',
      'last_items': 5,
    }

    GLOBAL_CONTEXT = {
      'asides': ['google_ads', 'github', 'google_plus', 'disqus_last_comments'],
      'google_analytics': google_analytics,
      'google_ads': google_ads,
      'github': github,
      'disqus': disqus,
    }


Options
-------

asides
~~~~~~

Sorted list of sections to be shown in the sidebar. You can choose these blocks:


- ``google_ads``: Will show Google adsense ads. You need to configure the ``google_ads`` variable as well.
- ``github``: Shows the latest updated GitHub repositories. You need to configure the ``github`` variable as well.
- ``disqus_last_comments``: Shows a list of the latest comments in disqus. You need to configure the ``disqus`` variable as well.
- ``google_plus``: Shows the ``+1`` banner. No additional configuration is required.


google_ads
~~~~~~~~~~

Dictionary with keys:

- ``pub``: Public advertisement id, taken from Google Adsense.
- ``slot``: Slot given by Google Adsense as well.
- ``width``: Advertisement width
- ``height``: Advertisement height


github
~~~~~~

- ``username``: Github username
- ``num_items``: Number of repositories to show. Default is 3.


disqus
~~~~~~

- ``username``: Disqus username
- ``num_items``: Number of items to be shown. Default is 5.


.. _`Octopress classic theme`: https://github.com/octopress/classic-theme
.. _`Nikola`: http://getnikola.com/
