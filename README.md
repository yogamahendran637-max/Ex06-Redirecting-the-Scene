# Ex06-Redirecting-the-Scene

## Aim:

To Redirecting the scene in the unity engine.


## Algorithm:

Step 1 :

To open the unity engine.

Step 2 :

Create a new 3D project.

Step 3 :

Create plane and name it as ground and create cube and name it as player.

Step 4 :

Add WinText in Hierarchy.

Step 5 :

Create a C# Script and name it as playercontroller and add the script to player.

Step 6 :

Use the R button to change the level 2

Step 7 :

Print the Output and end the program.





## Program:

```

using System.ComponentModel;
using System.Net.NetworkInformation;
using System.Runtime.CompilerServices;
using UnityEngine;
using UnityEngine.SceneManagement;

public class Movement : MonoBehaviour
{
    // Start is called once before the first execution of Update after the MonoBehaviour is created
    Rigidbody rb;
    public GameObject WinText;


    void Start()
    {
        rb = GetComponent<Rigidbody>();
    }

    // Update is called once per frame
    void Update()
    {
        if(Input.GetKeyDown(KeyCode.R))
        {
            SceneManager.LoadScene("Level2");
        }
    }
    private void OnTriggerEnter(Collider other)
    {
        if(other.gameObject.tag == "Cube")
        {
            Destroy(other.gameObject);
            WinText.SetActive(true);
        }
    }
}

```







## Output:



<img width="1017" height="508" alt="Screenshot 2026-09-19 010702" src="https://github.com/user-attachments/assets/f750f267-7988-4362-a478-060aa2af54b6" />



## Result:
The above C# coding is successfully redirecting the scene in the unity engine.











## Result:
