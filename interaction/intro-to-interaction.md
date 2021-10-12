# Interaction Basics

Interaction through player input is controlled through an Input class.

Easy shortcuts can be set up through the **Input Manager**.

Open your Input Manager through the taskbar > Edit > Project Settings...

This will open a new window/tab. Select Input Manager and twirl down the Axes menu.

![](<../.gitbook/assets/image (153).png>)

Twirl down one of the Axes listed to reveal default controls:

![Default settings for the Horizontal axis (for Keyboard)](<../.gitbook/assets/image (154).png>)

![Default settings for the Mouse X axis (for Mouse control)](<../.gitbook/assets/image (156).png>)

![Default settings for the Jump button (for Keyboard)](<../.gitbook/assets/image (155).png>)

This is where you can access the sensitivity for mouse, keyboard, and controller buttons as well as what buttons control the axis/button.

These can now be accessed through using Input.GetAxis() as a value that is positive or negative and Input.GetButton() as a bool value (true/false).

See the links below for coding specific scenarios:

{% content-ref url="keyboard-controls.md" %}
[keyboard-controls.md](keyboard-controls.md)
{% endcontent-ref %}

{% content-ref url="mouse-controls.md" %}
[mouse-controls.md](mouse-controls.md)
{% endcontent-ref %}

{% content-ref url="broken-reference" %}
[Broken link](broken-reference)
{% endcontent-ref %}

See more detail about user interaction in the [Unity documentation](https://docs.unity3d.com/Manual/Input.html).
