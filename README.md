# Line-Fitting-formula-derivation
The method aimed to fit line's general format Ax+By+C=0 with least-square algorithm.

In most of cases, people are used to fit y=kx+b that slope format.
However, sometimes we need to fit line's general format Ax+By+C=0 with more than 2 points.

The Loss is as follows, the distance sqr sum from these points to this line is expected to minimum 

![QianJianTec1719300374917](https://github.com/FengMu1995/Line-Fitting/assets/52693361/4e30e4b1-b3ed-4343-b5ae-93d6c3accbf2)

Now take the partial derivatives of F with respect to A, B, and C, and set them equal to zero.

![QianJianTec1719301003397](https://github.com/FengMu1995/Line-Fitting/assets/52693361/0b02a86a-2573-4849-8feb-d38baa3adb62)  (1)

![QianJianTec1719301209028](https://github.com/FengMu1995/Line-Fitting/assets/52693361/dd248823-d6bd-4f9f-83b1-ad6d2567e01c)  (2)

![QianJianTec1719301236221](https://github.com/FengMu1995/Line-Fitting/assets/52693361/7853569a-f639-4d15-8d7f-19b5a0405e4e)  (3)

some coefficients is defined:

   n = SUM 1,
   s = SUM x[i],
   t = SUM y[i],
   u = SUM x[i]^2,
   v = SUM x[i]*y[i],
   w = SUM y[i]^2,

unfold (1)(2)(3), we get
-v*A^2*B-s*A^2*C+(u-w)*A*B^2-2*t*A*B*C-n*A*C^2+v*B^3+s*B^2*C = 0, (4)

v*A^3+(w-u)*A^2*B+t*A^2*C-v*A*B^2-2*s*A*B*C-t*B^2*C-n*B*C^2 = 0,  (5)   

s*A+t*B+n*C = 0.                                                  (6)

from (6),
we get ![QianJianTec1719301570003](https://github.com/FengMu1995/Line-Fitting/assets/52693361/bcf2486d-7879-4e55-ac57-02584cd37994)  (7)

replace (7) into (4) or (5), we get 

(n*v-s*t)*A^2 + (s^2-t^2-n*u+n*w)*A*B - (n*v-s*t)*B^2 = 0.         (8)

futher simplify, 
A^2 + [(s^2-t^2-n*u+n*w)/(n*v-s*t)]*A*B - B^2 = 0.                 (9)

known,
s^2-t^2 = u-w
s*t=v

so (s^2-t^2-n*u+n*w)/(n*v-s*t) = w-u/v

(9) is converted to 
A^2 + [(w-u)/v]*A*B - B^2 = 0.                                      (10)


How to solve A, B
In some pro, A = w-u, B=v


because, it only compute A/B, instead A&B.








