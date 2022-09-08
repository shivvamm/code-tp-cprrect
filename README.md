# GeeksforGeeks Solutions (incorrect ones)

Foobar is a Python library for dealing with word pluralization.

## Leaders in an array

Given an array A of positive integers. Your task is to find the leaders in the array. An element of array is leader if it is greater than or equal to all the elements to its right side. The rightmost element is always a leader. 

```bash
Input:
n = 6
A[] = {16,17,4,3,5,2}
Output: 17 5 2
Explanation: The first leader is 17 
as it is greater than all the elements
to its right.  Similarly, the next 
leader is 5. The right most element 
is always a leader so it is also 
included.
```

## My solution

```cpp
class Solution{
    //Function to find the leaders in the array.
    public:
    vector<int> leaders(int a[], int n){
        // Code here
        vector<int> sol;
        int m=n-1;
        int s=0;
        int e=s+1;
        while(s<e){
           if(a[s]>a[e] && e != m){
               e++;
           }
        else if(a[s]>a[e] && e == m){
               sol.push_back(sol[s]);
               s++;
               e=s+1;
           }
           else{
               s++;
               e=s+1;
           }
           
        }
        for(int i=0;i<sol.size();i++){
            cout<<sol[i]<<" ";
        }
        
    }
};
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
