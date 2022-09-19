 class Solution {
    public ListNode deleteDuplicates(ListNode head) {
        if(head == null || head.next == null)
            return head;
        else{
            while(head.next != null && head.val == head.next.val){
                head = head.next;
            }
            ListNode p = head;
            while(p != null && p.next != null){
                if(p.val == p.next.val){
                    p.next = p.next.next;
                }
                else{
                    p = p.next;
                }
            }
            return head;
        }
