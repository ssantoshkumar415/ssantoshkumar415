var arr = new int[] { 1, 0, 2, 3, 0, 4, 5, 0 };
            int lastValue = 0;
            int count = 0;
            for (int i = 0; i < arr.Length - 1; i++)
            {
                if (arr[i] == 0)
                {
                    for (int j = i; j < arr.Length; j++)
                    {
                        int currentValue = arr[j];
                        if (count > 0)
                            arr[j] = lastValue;
                        lastValue = currentValue;
                        count++;
                    }
                    i++;
                }                
                count = 0;
            }
