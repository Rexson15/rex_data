def count_substring_non_overlapping(s1, s2):
    count = 0
    i = 0
    while i <= len(s1) - len(s2):
        if s1[i:i+len(s2)] == s2:
            count += 1
            i += len(s2)  # Move index ahead by length of s2 (non-overlapping)
        else:
            i += 1
    return count

# Example usage:
s1 = "ababababaaba"
s2 = "aba"
print(count_substring_non_overlapping(s1, s2))  # Output: 3
