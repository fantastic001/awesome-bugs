
This list is intended to list bugs I and others find in code. Maybe then we will be able to better understand where 
we make errors and how to generally fix source of them.


File operations
=================


EOF error
---------

You can reach EOF if you read multiple times. For example if you introduce new variable and forget to fix old code:

	char* x = read(1024);
	append_to_list(read(1024));
