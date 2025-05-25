//Reverse String
class Solution {
    public void reverseString(char[] s) {
        int lef=0,rig=s.length-1;
        while(lef<rig)
        {
            char tmp=s[lef];
            s[lef]=s[rig];
            s[rig]=tmp;
            lef++;
            rig--;
        }
    }
}
Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
*****************************************************
//Reverse Vowels of a String 
class Solution {
    public String reverseVowels(String s) {
        int start=0,end=s.length()-1;
        char ch[]=s.toCharArray();
        while(start<end)
        {
            if(!isvowels(ch[start]))
            {
                start++;
            }
            else if(!isvowels(ch[end]))
            {
                end--;
            }
            else
            {
            char t=ch[start];
            ch[start]=ch[end];
            ch[end]=t;
            start++;
            end--;
            }
        }
        return String.valueOf(ch);
    }
        private boolean isvowels(char ch)
        {
            if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'||ch=='A'||ch=='E'||ch=='I'||ch=='O'||ch=='U'){
                return true;
            }
            else{
                return false;
            }
        }
}
Input: s = "IceCreAm"

Output: "AceCreIm"
****************************************************************************************
Remove Duplicates from sorted Array
class Solution {
    public int removeDuplicates(int[] nums) {
        if (nums.length == 0) return 0;

        int i = 0;
        for (int j = 1; j < nums.length; j++) {
            if (nums[i] != nums[j]) {
                i++;
                nums[i] = nums[j];
            }
        }
        return i + 1;
    }
}
Input: nums = [0,0,1,1,1,2,2,3,3,4]
Output: 5, nums = [0,1,2,3,4,_,_,_,_,_]
************************************************************************************
Issubsequence
class Solution {
    public boolean isSubsequence(String s, String t) {
        int i = 0, j = 0;

        while (i < s.length() && j < t.length()) {
            if (s.charAt(i) == t.charAt(j)) {
                i++;
            }
            j++;
        }

        return i == s.length();
}
}
Input: s = "axc", t = "ahbgdc"
Output: false
