# Basic unit test notes
1. The test file must end with '_test' otherwise the test framework does not find the test file. You will get below error message:

`?   	github.com/Prithvipal/go-in-action/chapter9/basic_unit_test	[no test files]`

2. The test function must start with Test and then capitalized Name or _ with name. Both will work. Ex:
    ```
     TestDownload()
     Test_Donwload()
    ``` 

3. Below Command to run test case. If test case is successful, it will not print logs writen in test case. if testcase is failed the this command print detailed logs.

`go test`
    
Output on success:
```
ok  	github.com/Prithvipal/go-in-action/chapter9/basic_unit_test	9.963s
```

Output of fail:

```
--- FAIL: TestDownload (3.84s)
    first_test.go:15: Given the need to test downloading content.
    first_test.go:17: 	 When checking "http://www.goinggo.net/feedsx/posts/default?alt=rss" for status code "200"
    first_test.go:27: 		Should receive a "200" status. ✗ 404
FAIL
exit status 1
FAIL	github.com/Prithvipal/go-in-action/chapter9/basic_unit_test	3.846s

```

4. If you want to print test case log even if there is no error then you run below command


`go test v`

It will generate below output:
```
=== RUN   TestDownload
--- PASS: TestDownload (3.99s)
    first_test.go:15: Given the need to test downloading content.
    first_test.go:17: 	 When checking "http://www.goinggo.net/feeds/posts/default?alt=rss" for status code "200"
    first_test.go:25: 		Should receive a "200" status. ✓
PASS
ok  	github.com/Prithvipal/go-in-action/chapter9/basic_unit_test	3.992s

```
5. You don't need to write code to asserts. If you testcase executes `t.Error()` or `t.Fatal()`, the test case will fail else it will success. 
