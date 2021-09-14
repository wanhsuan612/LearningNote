### To read file
-------------------------
1. Open file
    ```
    f = open("file.txt")
    // or
    with open("file.txt) as f:
    ```
2. Read
    * Read a json file, which will return a dict
        ``` 
        content = json.loads(f) 
        ```
    * Read a txt file, which will return a string
        ```
        content = f.read()
        ```