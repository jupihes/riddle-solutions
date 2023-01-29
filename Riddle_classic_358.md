# https://fivethirtyeight.com/features/can-you-defeat-the-tiktok-meme/
```python

point_list = [20, 1, 18, 4, 13, 6, 10, 15, 2, 17, 3, 19, 7, 16, 8,
              11, 14, 9, 12, 5]
point_res = []
max_val = 0
for i in range(len(point_list)):
    point_res.append(0.5 * point_list[i] +
                     0.25 * point_list[divmod(i+1,20)[1]] +
                     0.25 * point_list[divmod(i-1,20)[1]])
    
    temp_val = 0.5 * point_list[i] +\
                     0.25 * point_list[divmod(i+1,20)[1]] +\
                     0.25 * point_list[divmod(i-1,20)[1]]
    if max_val < temp_val:
        max_val = temp_val
        
    # print(f'{divmod(i-1,20)[1]}, {divmod(i,20)[1]}, {divmod(i+1,20)[1]}')
    # print(f'{0.5*point_list[i] + 0.25 * point_list[divmod(i+1,20)[1]] +0.25 *    point_list[divmod(i-1,20)[1]]}')
    
    # print(f'{point_list[divmod(i-1,20)[1]]}, {point_list[i]}, {point_list[divmod(i+1,20)[1]]}')

for i, val in enumerate(point_res):
    if val == max_val:
        print(i)
        
```
