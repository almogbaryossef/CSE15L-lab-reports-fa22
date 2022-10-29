# **Lab Report 2**

## **Part 1**
The code for my SearchEngine is below.
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class StringHandler implements URLHandler {
    // The one bit of state on the server: a number that will be manipulated by
    // various requests.
    ArrayList<String> l = new ArrayList<String>();
    String s = "";
    
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Text: %s", s);
        } else if (url.getPath().equals("/addE")) {
            s += "e";
            return String.format("String added :)");
        } else {
            System.out.println("Path: " + url.getPath());
            if (url.getPath().contains("/add")) {
                String[] parameters = url.getQuery().split("=");
                if (parameters[0].equals("s")) {
                    l.add(parameters[1]);
                }
                return String.format("Added");
            }
            else if(url.getPath().contains("/search")) {
                String[] parameters = url.getQuery().split("=");
                if(parameters[0].equals("s")) {
                    String str = parameters[1];
                    String strs = "";
                    for(int i = 0; i < l.size(); i++) {
                        if(l.get(i).contains(str)) {
                            strs = strs + l.get(i) + " "; 
                        }
                    }
                    return String.format(strs);
                }
            }
            return "404 Not Found!";
        }
    }

    public void printArrayList(ArrayList<String> lst) {
        for(int i = 0; i < lst.size(); i++) {
            System.out.print(lst.get(i));
        }
    }
}

class  SearchEngine {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new StringHandler());
    }
}
```

We first enter in the terminal "javac SearchEngine.java and Server.java" in order to compile the program. We then enter "java SearchEngine 4893" (where 4893 is a random port number chosen for this exercise). This calls the main method in SearchEngine which takes in as an argument the number provided and creates a new server with that port and a StringHandler (which handles the path and any other parts of the link hat may be present), and returns the link to that server. Since there is no path (simply a hidden "/"), the handleRequest mathod in StringHandler simply returns "Text:". The link leads us to the following web:
![Image](https://user-images.githubusercontent.com/47935429/195967456-773e1b46-f297-45eb-acac-f52edfa28ee2.png)

At this point, we might decide that we want to add some fruit to the list. In order to do that, we would need to add a path and a query to the link that would be recognized by StringHandler. I designed my StringHandler so it has the handleRequest method, so when the path is "/add", the first argument (which should be a string) of the query would be added to a list ("l") that contains all fruit added. In order to confirm that the fuit has been added, for instance we can add "apple", the text returned is changed to "Added" every time we use "/add" correctly. Below is an example of adding the item "apple" to l, and we can see that instead of "Text:" there is "Added", which assures us that "apple" is now in l.
![Image](https://user-images.githubusercontent.com/47935429/195967494-100344d3-5875-4349-9989-27a1b4569011.png)

Using the method above, I kept the path "/add" and changed the parameter to be different fuit that I wanted to add to l: banana, pineapple, and another apple. Every time handleRequest is called (every time we reload the web), it goes through the possible valid paths until it finds "/add", and then it follows the steps for this "if" case. The first argument (second parameter, tecnically, since s is the first parameter) that is stored in parameters(1) is the item we add, and is changed every time we change the item (the String input in the query).
![Image](https://user-images.githubusercontent.com/47935429/195967503-947d10fa-311c-4ba6-a8a9-46ed5135c1ae.png)

Next, we can use the search path to get all items that contain a specific substring chosen by us. The String value may be in one or more of the items in "l", and the search "if" case would return all items that contain the given string. If none of the items contain the string, then no items will be returned. In the screenshot below I chose to use the String "app". The handleRequest method identifies the path as "/search", and then goes through the array list "l" and adds to a String variable all the items that contain the argument "app" (which is found in the query). Finally, it returns the String variable containing the appropriate items. Below is the result: 
![Image](https://user-images.githubusercontent.com/47935429/195967510-a2f7be5c-8670-4a78-a4e3-a04377c99066.png)

Also, to make sure that everything I have added is indeed in the list, I searched for all items that have the letter "a".
![Image](https://user-images.githubusercontent.com/47935429/195967517-d24fe52c-6d40-4369-81c4-33340b378662.png)


## **Part 2**
The first buggy method I chose is **averageWithoutLowest**. Below is a screenshot of the failure-inducing input (the test).
![Image](https://user-images.githubusercontent.com/47935429/195968156-dd4f4af7-28c2-42b9-8871-dca15c7d9019.png)

The symptom (output):
![Image](https://user-images.githubusercontent.com/47935429/195968301-4121bb7b-fc30-4263-b8ce-213490bd43e6.png)

The fixed code:

![Image](https://user-images.githubusercontent.com/47935429/195968353-227eafb4-b738-49f3-b91d-7c645248982d.png)

The symptom was that when the elements in the array are equal in value, the mean that was returned was zero. Since all of the numbers were equal to lowest, none of them were added to sum, so it remained zero. In order to fix this problem, I added another variable, "count." When the for-loop finds the lowest item, it sets count to 1. If count is set to 1, the item must be added to the sum regardless of whether it is equal to lowest. Therefore, only the first lowest item would not be added to the sum, in case there are multiple items with the same lowest value.
The average returned would be incorrect whenever there are duplicates of the lowest item in the list. 


The second buggy method I chose is **filter**. Below is a screenshot of the failure-inducing input (the test), as well as the symptom (output).
![Image](https://user-images.githubusercontent.com/47935429/195969051-ce79bb08-7b6d-41de-860b-25e7e3dc9c1f.png)

The fixed code:
![Image](https://user-images.githubusercontent.com/47935429/195969060-e37c3601-e276-4948-81c4-7995b2571320.png)

The symptom was that the first element in the list that was returned was the last element in the expected list. Since the original code of filter added the elements that satisfied the StringChecker to index 0, the order of the items in the array list was flipped. In order to fix this, I removed the index from the add method, and used the regular add(item) method which always adds the item to the end of the list.






Also this is what the addE method in my search engine does :)
![Image](https://user-images.githubusercontent.com/47935429/195969308-f1002a2a-373c-4088-9cb9-92757295667f.png)
