# algo_expert_solutions

# Two Number Sum
![](https://i.gyazo.com/a0baf7a1dee22c39fe6a7cf68919bedd.png)

## Solution 1

    public class Program {
    	public static int[] TwoNumberSum(int[] array, int targetSum) {
                int baseNumber = 0;
                int compareNumber = 0;
                for (int i = 0; i < array.Length; i++)
                {
                    baseNumber = array[i];
                    for (int b = i + 1; b < array.Length; b++)
                    {
                        compareNumber = array[b];
                        if (baseNumber + compareNumber == targetSum)
                            return new int[] { baseNumber, compareNumber };
                    }
                }
                return new int[0];
    	}
    }


## Solution 2 

    public class Program {
    	public static int[] TwoNumberSum(int[] array, int targetSum) {
                int iterationOutLoop = 0;
                int iterationInsideLoop = 0;
                foreach (int baseNumber in array)
                {
                    foreach (int compareNumber in array)
                    {
                        if(iterationOutLoop != iterationInsideLoop)
                        {
                            if(baseNumber + compareNumber == targetSum)
                            {
                                return new int[] { baseNumber, compareNumber };
                            }
                        }
                        iterationInsideLoop++;
                    }
                    iterationOutLoop++;
                    iterationInsideLoop = 0;
                }
                return new int[0];
    	}
    }

# Validate Subsequence
![](https://i.gyazo.com/91676fccebfd1bb14c0349c6577ef64a.png)

## Solution 1

    using System.Collections.Generic;
    
    public class Program {
    	public static bool IsValidSubsequence(List<int> array, List<int> sequence) {
                int sequenceNumberCheck = 0;
                for (int arrayIndexNumber = 0; arrayIndexNumber < array.Count; arrayIndexNumber++)
                {
                    if ((sequenceNumberCheck) != sequence.Count)
                    {
                        if (array[arrayIndexNumber] == sequence[sequenceNumberCheck])
                        {
                            sequenceNumberCheck++;
                        }
                    }
                }
                return sequenceNumberCheck == sequence.Count;
    	}
    }

# Find Closest Value In BST
![](https://i.gyazo.com/fb58b1f27dfc3fef643e6e5121c74977.png)

## Solution 1
