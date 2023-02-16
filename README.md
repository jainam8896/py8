m = int(input("Enter number of rows: "))

n = int(input("Enter number of columns: "))

#input of Matrix

matrix = []

for i in range(m):

    row = []

    for j in range(n):

        element = int(input(f"Enter element at index ({i}, {j}): "))

        row.append(element)

    matrix.append(row)

    

#Print Matrix

print("\nEntered Matrix")

for row in matrix:

        print(row)

#Sum of Each Row and Column

m = len(matrix)

n = len(matrix[0])

row_sum = [sum(row) for row in matrix]

col_sum = [sum([matrix[i][j] for i in range(m)]) for j in range(n)]

print("\nSum of each row",row_sum)

print("\nSum of each column",col_sum)

#find the highest and lowest from each row, each column, and the whole matrix

row_high = [max(row) for row in matrix]

row_low = [min(row) for row in matrix]

col_high = [max([matrix[i][j] for i in range(m)]) for j in range(n)]

col_low = [min([matrix[i][j] for i in range(m)]) for j in range(n)]

overall_high = max([max(row) for row in matrix])

overall_low = min([min(row) for row in matrix])

print("\nHighest From Rows",row_high)

print("\nLowest From Rows",row_low)

print("\nHighest From Columns",col_high)

print("\nLowest From Columns",col_low)

print("\nHighest From Matrix",overall_high)

print("\nLowest From Matrix",overall_low)

#find the sum of diagonal elements if the matrix is square matrix

m = len(matrix)

n = len(matrix[0])

if m != n:

    print("\nDiagonal Sum is not Possible because M!=N")

diagonal_sum = sum(matrix[i][i] for i in range(m))

print("\nDiagonal Sum : ",diagonal_sum)

#find the transpose of a matrix

transposed_matrix = [[matrix[j][i] for j in range(m)] for i in range(n)]

print("\nTransposed Matrix")

for row in transposed_matrix:

        print(row)
