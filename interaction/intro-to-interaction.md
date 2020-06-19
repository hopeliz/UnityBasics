# Interaction Basics

Interaction through player input is controlled through an Input class.

Easy shortcuts can be set up through the **Input Manager**.

Open your Input Manager through the taskbar &gt; Edit &gt; Project Settings...

This will open a new window/tab. Select Input Manager and twirl down the Axes menu.

![](../.gitbook/assets/image%20%28157%29.png)

Twirl down one of the Axes listed to reveal default controls:

![Default settings for the Horizontal axis \(for Keyboard\)](../.gitbook/assets/image%20%28164%29.png)

![Default settings for the Mouse X axis \(for Mouse control\)](../.gitbook/assets/image%20%28165%29.png)

![Default settings for the Jump button \(for Keyboard\)](../.gitbook/assets/image%20%28154%29.png)

This is where you can access the sensitivity for mouse, keyboard, and controller buttons as well as what buttons control the axis/button.

These can now be accessed through using Input.GetAxis\(\) as a value that is positive or negative and Input.GetButton\(\) as a bool value \(true/false\).

See the links below for coding specific scenarios:

{% page-ref page="keyboard-controls.md" %}

{% page-ref page="mouse-controls.md" %}

{% page-ref page="game-controllers.md" %}

See more detail about user interaction in the [Unity documentation](https://docs.unity3d.com/Manual/Input.html).

