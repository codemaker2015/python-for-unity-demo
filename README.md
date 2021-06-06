# Python for unity demo

Python for Unity facilitates Unity's interaction with various media and entertainment industry applications and ensures that you can integrate Unity into a broader production pipeline seamlessly. It allows access from Python to the full C# API of UnityEditor, UnityEngine, as well as your own C# APIs added to your Unity projects, and running Python code from within C#.

## Requirements
* Python 2.7.5 (64 bits) or later. The package does not work with Python 3.
* Unity 2019.3. We recommend installing the latest version of Unity 2019 via the Unity Hub; 2019.3 is the minimum.
* Used 2019.4.17f1 LTS

### Windows
* You must use Windows 10, patched to build 1803 or later.
* Install the software listed above in the default locations. When installing Python, make sure to check the option to add to the path is on.

## Setup
Python for Unity requires some manual installation:
* First, follow the installation instructions in the manual
* Next, install Python for Unity itself: Edit your Unity manifest.json file (in the Packages folder of your project) so that it starts with

```
{
  "dependencies": {
    "com.unity.scripting.python": "2.0.1-preview.2",
    ...
  }
}
```

## Sample Program
Create a script named HelloWorld.cs and attach it to the Main Camera.

```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
public class HelloWorld : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        Debug.Log("Unity: Hello World");
        print ("Python: Hello World");
    }
    // Update is called once per frame
    void Update()
    {
        
    }
}
```

## Output

![screenshot](https://github.com/codemaker2015/python-for-unity-demo/blob/master/Screenshots/screenshot1.png)

Also you can try like this,
* Run your application.
* Go to Window -> General -> Python Console
* Type the following code in the bottom window and click on the Execute button:

```
import UnityEngine
print ("Python: Hello World from python console")
UnityEngine.Debug.Log("Unity: Hello World from unity console")
```

![screenshot](https://github.com/codemaker2015/python-for-unity-demo/blob/master/Screenshots/screenshot2.png)
