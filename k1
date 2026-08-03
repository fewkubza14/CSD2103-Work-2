public class TwoSumSorted {

    public static boolean findPairBruteForce(int[] a, int k) {
        for (int i = 0; i < a.length; i++) {
            for (int j = i + 1; j < a.length; j++) {
                if (a[i] + a[j] == k) return true;
            }
        }
        return false;
    }

    public static boolean findPairRecursive(int[] a, int k, int left, int right) {
        if (left >= right) return false;
        int sum = a[left] + a[right];
        if (sum == k) return true;
        if (sum < k) return findPairRecursive(a, k, left + 1, right);
        return findPairRecursive(a, k, left, right - 1);
    }

    public static boolean findPairBinarySearch(int[] a, int k) {
        for (int i = 0; i < a.length; i++) {
            int complement = k - a[i];
            int left = i + 1, right = a.length - 1;
            while (left <= right) {
                int mid = left + (right - left) / 2;
                if (a[mid] == complement) return true;
                if (a[mid] < complement) left = mid + 1;
                else right = mid - 1;
            }
        }
        return false;
    }
}
