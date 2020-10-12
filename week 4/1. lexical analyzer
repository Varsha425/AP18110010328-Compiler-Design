%{
#undef yywrap
#define yywrap() 1
#include<stdio.h>
  int statements = 0;
  int ids = 0;
  int assign = 0;
  int rel = 0;
  int keywords = 0;
  int integers = 0; 
%}

DIGIT [0-9]
LETTER [A-Za-z]
TYPE int|char|bool|float|void|for|do|while|if|else|return|void|printf|scanf|main|include|stdio
PARAN "{"|"}"|"("|")"
RELOP "+"|"-"|"*"|"%"|"&"|"/"|"<"|">"
EXPR ","|";"|"\""|"."
%option yylineno
%option noyywrap

%%
{TYPE} {fprintf(yyout, " Keyword : %s\n", yytext);}
{RELOP} {fprintf(yyout, " Relational Operator : %s\n" , yytext);}
{PARAN} {fprintf(yyout, "Paranthesis : %s\n", yytext);}
{EXPR} {fprintf(yyout, " Supporters : %s\n", yytext);}
[0-9]+|[a-zA-Z][a-zA-Z0-9_]* {fprintf(yyout, "Identifier : %s\n" ,yytext);}
%%
void main(int argc, char **argv)
{
extern FILE *yyin, *yyout; 
  
    yyin = fopen("1.c", "r"); 
  
    yyout = fopen("Output2.txt", "w"); 
    
  yylex();
  printf("Successs! ! !\n");
}
