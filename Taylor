pkg load symbolic;

f=input(" Escriba la funcion ",'s');
syms x;
f=sym(f)

a=input("Digita el valor de a");
n=input("Digita el valor de n");
i=0;
y = sym(0);

while n>=i
   g=diff(f,x,i);
   termino=((subs(g,x,a))*((x-a)^(i)))/(factorial(i));
   y=y+termino;
   i=i+1;
  endwhile
 disp(y);
p=input("Digita el valor de x");
resultado=subs(y,x,p);
resultado=double(resultado);
valorTeorico=double(subs(f,x,p));
fprintf("Valor Teorico %.5f\n ",valorTeorico);
fprintf("Valor Experimental %.5f\n",resultado);
errorAbsoluto=abs((valorTeorico-resultado));
fprintf("Error Absoluto  %.5f\n ",errorAbsoluto);
errorRelativo=(errorAbsoluto/valorTeorico)*100;
fprintf("Error Relativo  %.5f\n ",errorRelativo);
% Dar valores para la grafica

f_eval = function_handle(f);
y_eval = function_handle(y);
values = 0:0.1:2*pi;
plot(values, f_eval(values), 'b', values, y_eval(values), 'r:');
xlabel('x');
ylabel('f(x)');
title('Función y Polinomio de Taylor');
legend('Función original', 'Polinomio de Taylor');
