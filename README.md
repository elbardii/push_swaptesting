# push_swaptesting

# Push_swap Tests - README

## Introduction

This README contains the tests required for the **push_swap** project. These tests will help evaluate the functionality of your program in various situations. Follow the instructions carefully to ensure your program is functioning correctly.

## Identity Test

### Test 1:
Run the following command:
```bash
$> ./push_swap 42
```
Expected result: The program should display nothing (0 instruction).

### Test 2:
Run the following command:
```bash
$> ./push_swap 2 3
```
Expected result: The program should display nothing (0 instruction).

### Test 3:
Run the following command:
```bash
$> ./push_swap 0 1 2 3
```
Expected result: The program should display nothing (0 instruction).

### Test 4:
Run the following command:
```bash
$> ./push_swap 0 1 2 3 4 5 6 7 8 9
```
Expected result: The program should display nothing (0 instruction).

### Test 5:
Run the following command:
```bash
$> ./push_swap 'Between 0 and 9 randomly sorted values chosen>'
```
Expected result: The program should display nothing (0 instruction).

## Simple Test

### Test 1:
Run the following command:
```bash
ARG="1 5 2 4 3"; ./push_swap $ARG | ./checker_OS $ARG
```
Expected result: The checker should display "OK", and the list of instructions from `push_swap` should not exceed 12. Ideally, the instruction list should be 8.

### Test 2:
Run the following command:
```bash
ARG="<5 random values>"; ./push_swap $ARG | ./checker_OS $ARG
```
Replace `<5 random values>` with five random valid values.
Expected result: The checker should display "OK", and the list of instructions from `push_swap` should not exceed 12. Repeat this test several times with different permutations.

## Middle Test

### Test:
Run the following command:
```bash
ARG="<100 random values>"; ./push_swap $ARG | ./checker_OS $ARG
```
Replace `<100 random values>` with 100 random valid values.
Expected result: 
- The checker should display "OK".
- The instruction list size should be less than 700 for 5 points, less than 900 for 4 points, less than 1100 for 3 points, less than 1300 for 2 points, and less than 1500 for 1 point.

Repeat this test several times with different permutations to ensure your program is not hardcoded to only pass this specific test.

## Advanced Test

### Test:
Run the following command:
```bash
ARG="<500 random values>"; ./push_swap $ARG | ./checker_OS $ARG
```
Replace `<500 random values>` with 500 random valid values.
Expected result:
- The checker should display "OK".
- The instruction list size should be less than 5500 for 5 points, less than 7000 for 4 points, less than 8500 for 3 points, less than 10000 for 2 points, and less than 11500 for 1 point.

Repeat this test several times with different permutations to ensure your program is not hardcoded to only pass this specific test.

## Checker Program - False Tests

### Test 1:
Run the following command:
```bash
$> ./checker 0 9 1 8 2 7 3 6 4 5
```
Then enter the following instruction list:
```bash
[sa, pb, rrr]
```
Expected result: The checker should display "KO".

### Test 2:
Run the following command with a valid list of your choice:
```bash
$> ./checker <valid list>
```
Then enter the following instruction list that doesn't sort the integers:
```bash
[sa, ra, pb, rra]
```
Expected result: The checker should display "KO".

Repeat this test several times with different lists and instructions to ensure your program handles all cases.

## Checker Program - Right Tests

### Test 1:
Run the following command:
```bash
$> ./checker 0 1 2
```
Then press CTRL+D without writing any instruction.
Expected result: The checker should display "OK".

### Test 2:
Run the following command:
```bash
$> ./checker 0 9 1 8 2
```
Then enter the following instruction list:
```bash
[pb, ra, pb, ra, sa, ra, pa, pa]
```
Expected result: The checker should display "OK".

Repeat this test several times with different lists and instructions to ensure your program handles all cases.

## Conclusion

These tests are designed to evaluate the core functionality of your push_swap program. Make sure your program passes all tests in each section to ensure it works properly under various scenarios.

