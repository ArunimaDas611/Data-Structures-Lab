void display(int arr[], int n) {
  for (int i = 0; i < n; i++) {
    printf("%d ", arr[i]);
  }
  printf("\n");
}
void merge(int arr[], int low, int mid, int high) {
  int i, j, k;
  int n1 = mid - low + 1;
  int n2 = high - mid;
  int lowArr[n1], highArr[n2];
  for (i = 0; i < n1; i++) {
    lowArr[i] = arr[low + i];
  }
  for (j = 0; j < n2; j++) {
    highArr[j] = arr[mid + 1 + j];
  }
  i = 0;
  j = 0;
  k = low;
  while (i < n1 && j < n2) {
    if (lowArr[i] <= highArr[j]) {
      arr[k] = lowArr[i];
      i++;
    } else {
      arr[k] = highArr[j];
      j++;
    }
    k++;
  }
  while (i < n1) {
    arr[k] = lowArr[i];
    i++;
    k++;
  }
  while (j < n2) {
    arr[k] = highArr[j];
    j++;
    k++;
  }
}
void splitAndMerge(int arr[], int low, int high) {
  if (low < high) {
    int mid = (low + high) / 2;
    splitAndMerge(arr, low, mid);
    splitAndMerge(arr, mid + 1, high);
    merge(arr, low, mid, high);
  }
}
