call_user_func(callable $callback, param, param);
eg:
1. 
	$func = function($arg1, $arg2) {
	    return $arg1 * $arg2;
	};
	var_dump(call_user_func($func, array(2, 4)));  // PHP Warning:  call_user_func_array() expects parameter 2 to be array, string given on line 3
	var_dump(call_user_func($func, 2, 4));	       // int(8)
	
	
call_user_func_array(callable $callback, array);
eg:
1.
	$func = function($arg1, $arg2) {
	    return $arg1 * $arg2;
	};

	var_dump(call_user_func_array($func, array(2, 4)));  // int(8)

2.
	namespace Foobar;

	class Foo {
	    static public function test($name) {
		print "Hello {$name}!\n";
	    }
	}

	// As of PHP 5.3.0
	call_user_func_array(__NAMESPACE__ .'\Foo::test', array('Hannes'));   // Hello Hannes!

	// As of PHP 5.3.0
	call_user_func_array(array(__NAMESPACE__ .'\Foo', 'test'), array('Philip')); // Hello Philip!

3. func_get_arg(int $key);
	function foo(){
	    $num = func_get_arg(2);

	    dd($num);  
	}
	foo(1,2,4);  // 4


   func_get_args(void);
	function foo(){
	    $num = func_get_args();

	    dd($num); 
	}
	foo(1,2,4); // array(1,2,4);

   func_num_args(void);
	function foo(){
	    $num = func_num_args();

	    dd($num); 
	}
	foo(1,2,4); // 3



