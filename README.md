Download Link: https://assignmentchef.com/product/solved-csi2120-lab-9-scheme
<br>
<h3>Exercise 1: Prefix Notation</h3>

Use Racket as an interactive Scheme calculator. Scheme uses prefix notation. Example:

(* 6 (- 10 5))

This expression will evaluate to 30 because 6 * (10 – 5) = 30.

<h4>Calculate the sum of the squares for the numbers 1 to 4. Hint: Your result should be 30.</h4>

<h4>Calculate both solutions to 2x^2 + 5x – 3 = 0.</h4>

<h4>Calculate the result of the sin(pi/4) cos(pi/3) + cos(pi/4) sin(pi/3)</h4>




<h3>Exercise 2: Local and Global Definitions</h3>

Global definition use define and local definition use let bindings.

<h4>Define a global constant</h4>

(define myFavorite 42)

Verify that you can use the definition.

<h4>Define locals with let</h4>

(let ((x 1) (y 2))  (+ x y))

Verify that after the evaluation x and y are no longer defined, e.g. by using (* x y)

<h4>Use a local let binding for the angles to calculate sin(pi/4) cos(pi/3) + cos(pi/4) sin(pi/3) again.</h4>




<h3>Exercise 3: Procedures</h3>

Lambda expressions create local procedures.

((lambda (x y) (+ x y)) 1 2)

This code defines the lambda and then uses it with the arguments 1 and 2.

<h4>Use a lambda with the angles as arguments to calculate sin(pi/4) cos(pi/3) + cos(pi/4) sin(pi/3) again.</h4>

We can also define global procedures.

(define foo (lambda (x y) (+ x y)))

<h4>Call the function foo with 1 and 2 as arguments.</h4>

Note that the syntax of Scheme follows strict form. The first entry in a list is treated as a function. Lists are written with round brackets. In fact all the above calculations used a list to express the calculation.

You can find more information in our textbook <a href="https://www.scheme.com/tspl4/">The Scheme Programming Language</a> by R. Kent Dybvig, especially, Section 2.5 Lambda Expressions.

<h4>Define a global function to calculate sin(alpha) cos(beta) + cos(alpha) sin(beta) with alpha and beta as parameters.</h4>




<h3>Exercise 4: Quadratic equation</h3>

Define a global function that finds both roots of a quadratic equation ax^2+bx+c = 0 with a,b,c as arguments. Note that you can calculate two solutions and return them as a list as follows:

(define foo (lambda (x y) (list (+ x y) (- x y))))

<h3>Exercise 5 and Quiz:</h3>

<em>Please hand-in the answer to this question on Virtual Campus at the latest by Friday 6:00pm! Your submission will only count if you also hand-in solutions to all of the exercises. However, Exercise 1 to 4 will not be graded.</em>

The following top-level define uses local lambda functions in its calculations (Half-angle trigonometric identity). Change the definition to instead use local let bindings.

(define (halfTrig theta)         (/ (* 2 ((lambda (x) (tan (/ x 2))) theta))          (+ 1 ((lambda (y) (* y y)) ((lambda (x) (tan (/ x 2))) 1.57)))))