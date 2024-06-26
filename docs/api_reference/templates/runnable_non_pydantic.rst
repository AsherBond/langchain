:mod:`{{module}}`.{{objname}}
{{ underline }}==============

.. NOTE:: {{objname}} implements the standard :py:class:`Runnable Interface <langchain_core.runnables.base.Runnable>`. 🏃


.. currentmodule:: {{ module }}

.. autoclass:: {{ objname }}

   {% block attributes %}
   {% if attributes %}
   .. rubric:: {{ _('Attributes') }}

   .. autosummary::
   {% for item in attributes %}
      ~{{ name }}.{{ item }}
   {%- endfor %}
   {% endif %}
   {% endblock %}

   {% block methods %}
   {% if methods %}
   .. rubric:: {{ _('Methods') }}

   .. autosummary::
   {% for item in methods %}
      ~{{ name }}.{{ item }}
   {%- endfor %}

   {% for item in methods %}
   .. automethod:: {{ name }}.{{ item }}
   {%- endfor %}

   {% endif %}
   {% endblock %}


.. example_links:: {{ objname }}
