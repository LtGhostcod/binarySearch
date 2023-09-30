# binarySearch
searching an entire array using binary search .public class Main
{
    public static int binary(int[] arr, int l, int r, int key){
        int mid = 0;
        while(l <= r){
            mid = l+(r-l)/2;
            
            if (arr[mid] == key)
            return mid;
            
            if(arr[mid] < key)
            l = mid+1;
            
            else{
            r = mid-1;
            }
            
        }
        return -1;
    }
	public static void main(String[] args) {
	    int[] arr = {1, 2, 3, 4, 5};
	    int l = 0;
	    int r = arr.length;
	    
	    int key = 4;
	    
	    int result = binary(arr, l, r, key);
	    
	    
	    if (result == -1){
	        System.out.println("Not found");
	    } 
	    else{
	        System.out.println("Found at index " +result);
	    }
	}
}

