# MergeSort in Python



def mergeSort(array):
    print("   ",array)
    if len(array) > 1:
    
        r = len(array)//2
        L = array[:r]
        M = array[r:]
        print(L,"   ",M)
        print()

        # Sort the two halves
        mergeSort(L)
        mergeSort(M)

        i = j = k = 0

        
        while i < len(L) and j < len(M):
            print(L,"        ",M,"   ",array)
            if L[i] < M[j]:
                array[k] = L[i]
                i += 1
            else:
                array[k] = M[j]
                j += 1
            k += 1

        
        while i < len(L):
            array[k] = L[i]
            i += 1
            k += 1

        while j < len(M):
            array[k] = M[j]
            j += 1
            k += 1
        
        print("after merging {} elements in a single array:{}".format(k,array))   


#Print the array
def printList(array):
    for i in range(len(array)):
        print(array[i], end=" ")
   


# Driver program
array = [6, 12, 5, 10, 9, 1]
print("array before sort:")
mergeSort(array)

print("Sorted array is: ")
printList(array)
