# Tarkov-Assembly-Cleaner
Fully cleans the tarkov assembly csharp. Including artifacts


```de4dot.exe C:\Users\void\Desktop\Assembly-CSharp.dll --un-name "!^<>[a-z0-9]$&!^<>[a-z0-9]__.*$&![A-Z][A-Z]\$<>.*$&^[a-zA-Z_<{$][a-zA-Z_0-9<>{}$.`-]*$" --strtyp delegate --strtok 0x0600B6A7 ```

last update on 12th April 2020

    de4dot Assembly-CSharp.dll --un-name "!^<>[a-z0-9]$&!^<>[a-z0-9]__.*$&!^<.[a-zA-Z0-9]{1,}>[a-z0-9]__.*$&![A-Z][A-Z]\$<>[0-9]__[a-zA-Z0-9]{1,}$&^[a-zA-Z_<{$][a-zA-Z_0-9<>{}$.`-]*$" --strtyp delegate --strtok 0x0600B71F
    



A quick way to look up the TOKEN with dnSpy:
01- Open dnSpy
02-Load Assembly-CSharp.dll  //Assembly Cleaner for Escape From Tarkov!-dnspy-1-png
03-Press Ctrl+Shift+K for Assembly Search
04-Type in Assembly.GetExecutingAssembly  //-Assembly Cleaner for Escape From Tarkov!-dnspy-2-png
05-Pick one with type of SystemReflection.Assembly
06-Right-click on it and pick Analyze  //Assembly Cleaner for Escape From Tarkov!-dnspy-3-png
07- Expand Used By
08- Look for \uXXXX:..cctor    //Assembly Cleaner for Escape From Tarkov!-dnspy-4-png
09-Pick one that is in the Assembly-CSharp.dll
10-Method immediately after it containing the GetData call is the method  //Assembly Cleaner for Escape From Tarkov!-dnspy-5-png


refere: 
https://www.unknowncheats.me/forum/escape-from-tarkov/381749-assembly-cleaner-escape-tarkov.html
