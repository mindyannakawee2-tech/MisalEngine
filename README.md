<img width="1000" height="1000" alt="logo" src="https://github.com/user-attachments/assets/f5944f4b-6514-4945-b86d-6172516f0bb0" />
A C# Game Framework

### Set Up
You don't need to set up Misal because it's a full project template
but make sure you scripted in Main.cs

# Scripting
### Graphics
```cs
// Color
misal.Graphics.Color(r, g, b, a);
// Clear

misal.Graphics.Clear(r, g, b, a); // for custom clear since the engine has auto clear
// Rectangles
misal.Graphics.Rect(x, y, width, height);
// Line
misal.Graphics.RectLine(x, y, width, height);
misal.Graphics.Line(x1, y1, x2, y2);
// Text
misal.Graphics.Text(font, x, y, "Hello");
// Sprites
var sprite = misal.Graphics.LoadImage("pathName/pathName/pathName/.../imageName.png");
sprite.Draw(x, y);
sprite.Draw(x, y, sx, sy); // for changing size in game
sprite.Dispose();
sprite?.Dispose();// Check if there is sprite
// Window Icon
misal.Graphics.DisplayIcon = iconSprite;
```

### Text & Fonts
```cs
// Load Font
var font = new Font("pathName/pathName/pathName/.../fontName.ttf", size);
// Disposing
font.Dispose();
// Check Object Disposing
font?.Dispose();
```

### Audio
```cs
// Load Audio
var audio = misal.AudioLoader.Load("pathName/pathName/pathName/.../audioName.mp3");
// Play
audio.Play(loop: false);
// Pause
audio.Stop();
// Resume
audio.Resume();
// Stop
audio.Stop();
// Disposing Again
audio.Dispose();
audio?.Dispose(); // for checking the instance
```
### Input
```cs
misal.Input.IsDown("KeyName");
misal.Input.IsUp("KeyName");
misal.Input.IsPressed("KeyName");
misal.Input.IsReleased("KeyName");
```

# Requirements
https://dotnet.microsoft.com/en-us/download/dotnet/thank-you/sdk-10.0.203-windows-x86-installer
this is .NET 10.0
https://github.com/edwardgushchin/SDL3-CS
this is SDL3 for C#
