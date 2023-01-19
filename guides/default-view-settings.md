# Default view settings

In Kumu, **default view settings** is your one-stop-shop for adjusting the underlying settings in your [view](/guides/views.md). Templates, layouts, default element and connection styles, and more can all be changed with default view settings.

## Change default view settings in the Basic Editor

You can find the **Default view settings** tool in the [Basic Editor](/overview/view-editors.md#basic-editor) by clicking the settings icon ![](/icons/sliders-h.svg) on the right side of your map, then clicking **MORE OPTIONS** and selecting **Customize view defaults**.

![Default view settings](/images/basic-editor-default-settings.png)

The tool has up to six sections, depending on the [template](/guides/templates.md) and [layout](/guides/layouts.md) you're using: Template settings, Element defaults, Connection defaults, Font defaults, Layout settings, and General settings.


#### Template settings

This section, which is only available for the systems, stock and flow, and causal loop templates, allows you to tweak things like same/opposite connection color, connection labels, and more.


#### Element, Connection, and Font defaults

These three sections allow you to change colors, sizes, widths, and other styles for all your elements and connections. Font defaults will apply to loops, as well.

Note that any [decorations](/guides/decorate.md) you have created will override your default settings.

#### Layout settings

 Layout settings are available when you are using the force-directed layout on your map. For more information on how to use this section, check out our [full guide on the force-directed layout](/guides/layouts/force-directed.md).

#### General settings

The General settings section allows you change your theme, template, quality, and layout.

**Theme** can be either light or dark. The dark theme is great for big screens in dark rooms!

**Template** allows you to choose one of Kumu's pre-built [templates](/guides/templates.md).

**Quality** can be either high or low/fast. High quality gives you full access to Kumu's suite of decorations, but it will run slowly on very large maps. Low/fast, on the other hand, restricts your access to different decorations, but it helps large maps to load and animate much more quickly.

**Layout** allows you to choose between the [fixed layout](/guides/layouts/fixed.md) (select "off" from the dropdown) or [force-directed layout](/guides/layouts/force-directed.md).


## Change default view settings in the Advanced Editor

In the [Advanced Editor](/overview/view-editors.md#advanced-editor), you can use the `@settings` at-rule to change default view settings:

```
@settings {
  property: value;
}
```

Replace `property` with any property from the [settings reference](/guides/settings-reference.md), and replace `value` with any valid value for that property, as described in the settings reference.



