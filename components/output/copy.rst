Copy Output
===========

.. seo::
    :description: Instructions for setting up a copy output in ESPHome.
    :image: content-copy.png

The ``copy`` output platform allows you to copy an output to other platforms,
so that they are always kept in sync.

It supports two types of outputs: ``binary`` and ``float`` with the type parameter
- the former only being for GPIO output platforms.

.. code-block:: yaml

    # Example configuration entry
    output:
      - platform: copy
        id: copy_output
        outputs:
          - my_first_output
          - my_second_output

      # Example for target outputs
      - platform: esp8266
        id: my_first_output
        pin: D1
      - platform: esp8266
        id: my_second_output
        pin: D2

    # Example usage in a light
    light:
      - platform: monochromatic
        output: copy_output
        name: "Kitchen Light"

Configuration variables:
------------------------

- **outputs** (**Required**, list of :ref:`config-id`): A list of IDs that this output
  should control.
- **type** (**Required**, string): The type of output to control, ``binary`` or ``float``.
  Defaults to ``float``.
- **id** (**Required**, :ref:`config-id`): The id to use for this output component.
- All other options from :ref:`Output <config-output>`.

See Also
--------

- :apiref:`output/copy_output.h`
- :ghedit:`Edit`

.. disqus::
