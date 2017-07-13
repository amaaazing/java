import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collections;
import java.util.List;

public class SplitList {

	// chops a list into non-view sublists of length L
	public static <T> List<List<T>> chopped(List<T> list, final int L) {
		final int N = list.size();		
		if (list == null || N == 0 || L < 1) {
			return null;
		}
	    List<List<T>> parts = new ArrayList<List<T>>();
	    
	    for (int i = 0; i < N; i += L) {
	        parts.add(new ArrayList<T>(
	            list.subList(i, Math.min(N, i + L)))
	        );
	    }
	    return parts;
	}

	public static void main(String[] args) {
		List<Integer> numbers = Collections.unmodifiableList(
			    Arrays.asList(5,3,1,2,9,5,0,7)
			);
			List<List<Integer>> parts = chopped(numbers, 3);
			System.out.println(parts); // prints "[[5, 3, 1], [2, 9, 5], [0, 7]]"
			parts.get(0).add(-1);
			System.out.println(parts); // prints "[[5, 3, 1, -1], [2, 9, 5], [0, 7]]"
			System.out.println(numbers); // prints "[5, 3, 1, 2, 9, 5, 0, 7]" (unmodified!)
	}

}
