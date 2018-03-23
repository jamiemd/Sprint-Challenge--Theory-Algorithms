Exercise I

a. O(N) since the change is linear

b. O(N2) since it's exponential

c. O(N2) since it's exponential

d. O(N) since it's exponential

e. O(N4) since there are 4 four loops

f. O(2N) since it's recursion

g. O(N) since the change is linear


Exercise II

a.
const insert = (compare = (a, b) => a < b, item, list) => {
    let result = [];
    let inserted = false;
    for (let i = 0; i < list.length; i += 1) {
        const val = list[i];
        if (compare(val, item)) {
            result.push(val);
        } else {
            result = result.concat(item, list.slice(i));
            inserted = true;
            break;
        }
    }
    return inserted ? result : result.concat(item);
};

b.
int eggDrop(int n, int k)
{
    if (k == 1 || k == 0)
        return k;
 
    if (n == 1)
        return k;
 
    int min = INT_MAX, x, res;
 
    for (x = 1; x <= k; x++)
    {
        res = max(eggDrop(n-1, x-1), eggDrop(n, k-x));
        if (res < min)
            min = res;
    }
 
    return min + 1;
}


Exercise III

a. O(n2): It would have to go through the entire array even though everything is in order. 

b. O(nLogn): The growth curve peaks at the beginning but then gradually decreases while going through the array since there are less items to compare starting at the median. 






