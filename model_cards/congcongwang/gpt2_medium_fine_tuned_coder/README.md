### Autocoder: A basic and simple tool for code auto completion, fine-tuned from the pytorch pre-trained GPT-2 variants offered by the awesome 🤗 transformers library.

[This repository](https://github.com/wangcongcong123/auto_coding) contains the code for fine-tuning this model.

For knowing the details of dataset construction and pre-training process, refer to [this blog](https://wangcongcong123.github.io/AutoCoder/)


### Generative examples
Good Python generation examples by fine-tuned GPT2-medium
```python
-------------Example 1--------------------------------------
Context code: def factorial
Generated: 
def factorial(n):
    return 1 if n == 1 else n * factorial(n - 1)

--------------Example 3-------------------------------------
Context code: def quick_sort(collection)
Generated:
def quick_sort(collection):
    """
    >>> quick_sort([0, 5, 3, 2, 2])
    [0, 2, 2, 3, 5]
    >>> quick_sort([])
    []
    >>> quick_sort([-2, -5, -45])
    [-45, -5, -2]
    """
    length = len(collection)
    if length <= 1:
        return collection
    else:
        # Use the last element as the first pivot
        pivot = collection.pop()
        # Put elements greater than pivot in greater list
        # Put elements lesser than pivot in lesser list
        greater, lesser = [], []
        for element in collection:
            if element > pivot:
                ...
```
Good Java generation examples by fine-tuned GPT2-medium

```javascript
--------------Example 1-------------------------------------
Context code: Scanner input= new Scanner(System.in)
Generated:
Scanner input= new Scanner(System.in)
System.out.println("Enter the Octal number: ");
// Take octal number as input from user in a string
String oct = input.next();

--------------Example 2-------------------------------------
Context code: private static int CountCharacters(String str)
Generated:
private static int CountCharacters(String str) {
        return str.replaceAll("\\s", "").length();
}
```
\* Although some generated examples look good, it needs to take a grain of salt to judge the model's actual performance. The model may simply **"remembers"** existing code in the training set well.
