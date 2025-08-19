bool carPooling(int** trips, int tripsSize, int* tripsColSize, int capacity) {
    int diff[1002] = {0}; 
    
    
    for (int i = 0; i < tripsSize; i++) {
        int numPassengers = trips[i][0];
        int from = trips[i][1];
        int to = trips[i][2];
        diff[from] += numPassengers;   
        diff[to + 1] -= numPassengers; 
    }
    
    
    int count = 0;
    for (int x = 0; x <= 1000; x++) {
        count += diff[x];
        if (count > capacity) {
            return false; 
        }
    }
    
    return true; 
}
