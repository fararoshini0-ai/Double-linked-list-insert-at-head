# Double-linked-list-insert-at-head
Implemented a Doubly Linked List program in Java to insert a new node at the head of the list.
public class doubleLL
{
    static class Node 
    {
        int val;
        Node next;
        Node prev;
        Node(int val)
        {
            this.val=val;
        }
    }
    public  static void display(Node random)
    {
       Node temp=random;
       while(temp.prev!=null)
       {
           temp=temp.prev;
       }
       while(temp!=null)
       {
        System.out.print(temp.val+" ");
        temp=temp.next;
        
       }
       System.out.println();
    }
    public static Node insertAtHead(Node head,int x)
    {
        Node t=new Node(11);
        t.next=head;
        head.prev=t;
        head=t;
        return head;
    }
    public static void main (String[] args) {
        Node a=new Node(22);
        Node b=new Node(23);
        Node c=new Node(24);
        Node d=new Node(25);
        Node e=new Node(26);
        a.prev=null;
        a.next=b;
        b.prev=a;
        b.next=c;
        c.prev=b;
        c.next=d;
        d.prev=c;
        d.next=e;
        e.prev=d;
        e.next=null;
        display(c);
        Node newhead=insertAtHead(a,11);
       
        display(newhead);
        
    }
        
    }
    
