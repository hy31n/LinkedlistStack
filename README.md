# LinkedlistStack
```C#
public class StackUsingLinkedlist
```
StackUsingLinkedlist 클래스를 만든다.     

```C#
private class Node
       {
           public int data;
           public Node link;
       } 
```
int 타입 data, Node 타입 link 변수가 포함된 Node 클래스를 만든다.  

```C#
Node top;
```
Node 타입 전역변수 top를 선언한다.  

```C#
public StackUsingLinkedlist() { this.top = null; } 
```
top이 null인 스택 구조를 만든다.

```C#
public void push(int x)

        {
            Node temp = new Node();

            if (temp == null)
            {
                Console.Write("\nHeap Overflow");
                return;
            }

            temp.data = x;
            temp.link = top;
            top = temp;

        }
```        
새 노드를 임시 생성하고 메모리를 할당한다.   
스택이 가득 찼는지 확인하고 다음 data를 삽입한다.  
데이터(x)를 임시 데이터 필드로 초기화 한다.  
임시 링크에 top를 삽입한다.  
top 참조를 업데이트한다.

```C#
public bool isEmpty() { return top == null; }
public int peek()
        {
            if (!isEmpty())
            {
                return top.data;
            }
            else
            {
                Console.WriteLine("Stack is empty");
                return -1;
            }
        }       
```  
스택이 비어 있는 여부를 판단하는 함수를 만든다.

```C#
 public void pop() 

        {
            if (top == null)
            {
                Console.Write("\nStack Underflow");
                return;
            }
            top = (top).link;
        }
```
스택 최상위 data를 삭제하는 함수를 만든다.  
```C#
public void display()
        {
            if (top == null)
            {
                Console.Write("\nStack Underflow");
                return;
            }
            else
            {
                Node temp = top;
                while (temp != null)
                {
                    Console.Write(temp.data);
                    temp = temp.link;
                    if (temp != null)
                        Console.Write(" -> ");
                }
            }
        }
``` 
node들을 print 해주는 함수를 만든다.

# 실행 화면
![Stack실행화면](https://user-images.githubusercontent.com/102163109/227840752-db3f7eeb-f5de-4d30-9ee3-65ada23cba0e.PNG)
