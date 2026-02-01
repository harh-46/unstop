# unstop
POTD **Feb-1**



solution



def count_clear_views(peaks, limit):
    # User will implement the logic here
    # Parameters:
    # - heights: list of integers representing the heights of peaks
    # - K: maximum number of tourists
    # Returns:
    # - int: maximum number of tourists with a clear sunset view
    tallest_so_far=peaks[0]
    visible=1

    for height in peaks[1:]:
        if height>tallest_so_far:
            tallest_so_far=height
            visible+=1
    return  visible if visible < limit else limit

if __name__ == "__main__":
    n, K = map(int, input().split())
    peaks = list(map(int, input().split()))
    answer = count_clear_views(peaks, K)
    print(answer)
