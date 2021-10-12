# Creating Custom Components and Scripts

## Creating a Custom Component / Script Through the Inspector

Sometimes, you have to make your own component. These are called Scripts and use C# and Unity's libraries and classes. These built-in libraries and classes allow you to use very little script compared to coding everything by scratch.

To add a custom component through the [Inspector](../../the-unity-interface/the-tabs/inspector-tab.md), click the **Add Component** button.

![](<../../.gitbook/assets/image (83).png>)

Scroll down to **New script**.

![](<../../.gitbook/assets/image (90).png>)

This will ask you for the name of your script and will let you know if it matches the name of an existing script."

{% hint style="danger" %}
Script names should:\
1\. Have no spaces\
2\. Use only letters and numbers\
3\. Not start with a number\
4\. Use "Pascal casing" (capitalize each word)\
5\. Be descriptive

Not following these "rules" could break scripts.
{% endhint %}

![](<../../.gitbook/assets/image (91).png>)

Type in the name of your script and you are absolutely sure that's what you want to name it, click the Create and Add button. 

![](<../../.gitbook/assets/image (92).png>)

The script will now appear in the [Project ](../../the-unity-interface/the-tabs/project-tab.md)window, in the Assets folder, the list of components, and in the Inspector.

![](<../../.gitbook/assets/image (93).png>)

![](<../../.gitbook/assets/image (94).png>)

![](<../../.gitbook/assets/image (95).png>)

The script can now be edited in the IDE/code editor set up with Unity (usually Visual Studio or MonoDevelop).

Please see the [Coding Basics](../../coding-basics/intro-to-scripts.md) section for more information on the actual scripting.

### Creating a Script Through the Project Tab

Add a C# Script using the Assets > Create menu or right-clicking in the Project window.

This will create a script asset within the current folder with the name highlighted ready to change. 

{% hint style="danger" %}
Script names should:\
1\. Have no spaces\
2\. Use only letters and numbers\
3\. Not start with a number\
4\. Use "Pascal casing" (capitalize each word)\
5\. Be descriptive

Not following these "rules" could break the script.
{% endhint %}

Press the ENTER key to confirm the name.

The script can now be edited in the IDE/code editor set up with Unity (usually Visual Studio or MonoDevelop).

After editing, the script will need to be added to the game object or asset for it to run.

{% hint style="danger" %}
Renaming scripts in the Project window will require additional renaming within the script. The script will not automatically update.
{% endhint %}

Please see the [Coding Basics](../../coding-basics/intro-to-scripts.md) section for more information on the actual scripting.

{% hint style="warning" %}
REMEMBER: Add the script to a game object in the scene. It will not work if it does not exist in the game.
{% endhint %}

{% content-ref url="../../select/components/" %}
[components](../../select/components/)
{% endcontent-ref %}

{% content-ref url="../../delete/components/" %}
[components](../../delete/components/)
{% endcontent-ref %}

