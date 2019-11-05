# Basic unit test notes
1. The test file must end with '_test' otherwise the test framework does not find the test file. You will get below error message:

`?   	github.com/Prithvipal/go-in-action/chapter9/basic_unit_test	[no test files]`

2. The test function must start with Test and then capitalized Name or _ with name. Both will work. Ex:
    ```TestDownload()
    Test_Donwload()```
    
