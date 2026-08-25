# Grading Students

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

HackerLand University has the following grading policy:

* Every student receives a $grade$ in the inclusive range from $0$ to $100$.
* Any $grade$ less than $40$ is a failing grade. 

Sam is a professor at the university and likes to round each student's $grade$ according to these rules:

* If the difference between the $grade$ and the next multiple of $5$ is less than $3$, round $grade$ up to the next multiple of $5$.
* If the value of $grade$ is less than $38$, no rounding occurs as the result will still be a failing grade.

**Examples**

- $grade = 84$ round to $85$ (85 - 84 is less than 3)  
- $grade = 29$ do not round (result is less than 38)  
- $grade = 57$ do not round (60 - 57 is 3 or higher)   

Given the initial value of $grade$ for each of Sam's $n$ students, write code to automate the rounding process.   

**Function Description**  

Complete the function $gradingStudents$ with the following parameter(s):  

- $int\ grades[n]$: the grades before rounding  

**Returns**

- $int[n]$: the grades after rounding

**Input Format**

The first line contains a single integer, $n$, the number of students. 		
Each line $i$ of the $n$ subsequent lines contains a single integer, $grades[i]$.

**Constraints**

* $ 1 \le n \le 60 $
* $ 0 \le grades[i] \le 100 $

**Output Format**

## Solution

**Language:** Java  
**Runtime:** N/A  
**Memory:** N/A  
**Submitted:** 2026-08-25T04:12:59.457Z  

```java
                } else {
                    result.add(grade);
                }
            }
        }

        return result;
    }

    public static void main(String[] args) throws IOException {

        BufferedReader br =
            new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(br.readLine().trim());

        List<Integer> grades = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            grades.add(Integer.parseInt(br.readLine().trim()));
        }

        List<Integer> result = gradingStudents(grades);

        for (int grade : result) {
            System.out.println(grade);
        }
    }
}
```

---

[View on HackerRank](https://www.hackerrank.com/challenges/grading/problem)