# CUnit

Simple and automatic single header C unit testing tool.

Take a look at the example.

### Syntax:
```c
#include "../cunit.h"

TEST(test_one) {
	ASSERT_EQUAL_STR("bello", "bello");
}

TEST(test_two) {
	ASSERT_EQUAL_INT(10, 10);
}

//SEG FAULT
TEST(test_three) {
	int *p = NULL;
	*p = 42;
	ASSERT_EQUAL_INT(42, *p);
}

//THIS TEST WILL FAIL
TEST(test_four) {
	ASSERT_EQUAL_STR("Hello", "Hell");
}

int main() {
	run_tests();
	return 0;
}
```

### Basic Usage:
![Alt text](resources/tests.png)

### Compatibility
This tool uses the \_\_attribute\_\_((constructor)) extension, so make sure that your compiler supports it.
