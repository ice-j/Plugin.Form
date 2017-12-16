# Form Plugin
Change the keyboard OK button accross platform from your shared project by wrapping the controls with a `<Form>` like in HTML

**Build Status**: comming soon
**NuGets**

|Name|Info|
| ------------------- | :------------------: |
|Form.Plugin|coming soon|
|MonkeyCache - Dev|coming soon|

**Platform Support**

Form Plugin is a .NET Standard 2.0 library, but has some platform specific tweaks for properly handling the keyboard changes in a `<Form>`.

|Platform|Version|
| ------------------- | :------------------: |
|Xamarin.iOS|iOS 8+|
|Xamarin.Mac|- Not Supported -|
|Xamarin.Android|API 14+|
|Windows 10 UWP|10.0.16299+|
|.NET Core|2.0+|
|ASP.NET Core|2.0+|
|.NET|4.6.1+|

### What is Form Plugin?

The goal of Form Plugin is to enable developers to easily change the keyboard `Done` button from a shared project so you don't have to write platform specific code to create beautiful CRUD forms.

For an instance, you want to make a login form, the XAML code will look something like this:

```xaml
<Form DoneCommand='{Binding DoneCommand}'>
    <Entry Form.Keyboard='Next' />
    <Entry Form.Keyboard='Done' />
    <Button Text="Login" Command='{Binding DoneCommand}' />
</Form>
```

## Setup

Not required, but if the linker somehow strips the code, you can call `Plugin.Form.Init()` on any platform.
