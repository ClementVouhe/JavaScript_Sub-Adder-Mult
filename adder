/*
*	sub method which subtracts two arguments
*	Author : Vouhé Clément
*/

function sub(a){ 
	return function(b){
		return a-b;
	}
}

/*
*   TEST Sub
*/

sub(0)(0); // 0
sub(2)(1); // 1
sub(2)(2); // 0
sub(2)(4); // -2

/*
*	adder method which addition x arguments and return the result
*	Author : Vouhé Clément
*/

function adder(){
	var args = Array.prototype.slice.call(arguments); // Recovery of all arguments in a table
	return function(v){
		var result = 0;
		args.forEach(function(value, i){ // ForEach on the table of arguments
			result+=args[i](v);
		});
		return result;
	}
}

/*
*	mult method which multiply two arguments and return the result
*	Author : François-Guillaume Ribreau
*/

function mult(v){
	return function(e){
		return v*e;
	}
}

/*
*   TEST adder
*/

adder()(0); // 0
adder()(1); // 0
adder(mult(2))(1); // 2
adder(mult(2), mult(2))(1); // 4
adder(mult(2), mult(2), mult(2))(1); // 6
adder(mult(2), sub(2), mult(2))(1); // 5
