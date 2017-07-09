Program Pzim ;
 var
	   z,y,x,w,Num,cnt,start:integer;
    guess:array[1..20] of integer;
    linha,coluna:integer;

procedure space;
Begin
writeln;
writeln;
writeln;	

end;	
procedure quit;
Begin																									
	writeln;
	writeln;
	writeln;
	writeln('Fim do jogo aperter <Enter> para encerrar!');
	readkey;	
end;
	
Begin
	z:=1;
	gotoxy(1,1);
	textcolor(blue);
	write('                           Bem vindo ao jogo das cores                      ');
	space;
      //barra vermelha superior
	linha:=5;
	coluna:=15;
	gotoxy(coluna,linha);
	for coluna:=15 to 65 do 
	begin
	gotoxy(coluna,linha);
	textcolor(red);
	write(#219);
	end;
	     //barra vermelha inferior
	linha:=35;
	coluna:=15;
	gotoxy(coluna,linha);
	for coluna:=15 to 65 do 
	begin
	gotoxy(coluna,linha);
	textcolor(red);
	write(#219);
	end;
	 //barra vermelha lateral direita
	linha:=5;
	coluna:=15;
	gotoxy(coluna,linha);
	for linha:=5 to 35 do  
	begin
	gotoxy(coluna,linha);
	textcolor(red);
	write(#219,#219);
	end;
	    //barra vermelha lateral esquerda
	linha:=5;
	coluna:=65;
	gotoxy(coluna,linha);
	for linha:=5 to 35 do  
	begin
	gotoxy(coluna,linha);
	textcolor(red);
	write(#219,#219);
	end;
	
	//texto dentro da red box
	
	linha:=10;
	coluna:=20;
	gotoxy(coluna,linha);
	textcolor(white);
	writeln('Regras:A tela ira mudar de cor 14 veses');
	gotoxy(coluna,11);
	writeln('  Advinhe a cor que vai estar no final');
	gotoxy(coluna,12);
	writeln('Entre as seguintes cores(podem repitir):');
	gotoxy(27,13);
	textcolor(blue);
	write('1|Azul|');
	
	gotoxy(27,14);
	textcolor(red);
	write('2|Vermelho claro|');
	
	gotoxy(27,15);
	textcolor(lightblue);
	write('3|Azul claro|');
	
	gotoxy(27,16);
	textcolor(yellow);
	write('4|Amarelo|');
	
	gotoxy(27,17);
	textcolor(green);
	write('5|Verde|');
	
	gotoxy(27,18);
	textcolor(cyan);
	write('6|Ciano|');
	
	gotoxy(27,19);
	textcolor(brown);
	write('7|Marrom|');
	
	gotoxy(27,20);
	textcolor(lightgreen);
	write('8|Verde claro|');
	
	gotoxy(27,21);
	textcolor(8);
	write('9|cinza escuro|');
	
	gotoxy(27,22);
	textcolor(white);
	write('10|Branco|');
	
	gotoxy(27,23);
	textcolor(7);
	write('11|Cinza Claro|');
	
	gotoxy(27,24);
	textcolor(13);
	write('12|magenta claro|');
	
	gotoxy(27,25);
	textcolor(5);
	write('13|magenta escuro|');
	
	gotoxy(27,26);
	textcolor(4);
	write('14|vermelho escuro|');
	
	gotoxy(20,28);
	textcolor(white);
	writeln('Escolha uma Cor Referente aos numeros acima:');
	gotoxy(20,29);
	repeat
	gotoxy(20,29);
	readln(start);
	until ((start <=14) and (start >=1));
	guess[z]:=start;
	
	clrscr;
	randomize;
	   //mudar a cor da tela
	for y:=1 to 14 do
	begin
	 delay(500);
	 x:=random(14)+1;
	 
	 if x = 1 then 
	 	begin
	 	textbackground(blue);
	 	 clrscr;
	  end;
	  
	  if x = 2 then
	 	begin
	 	textbackground(red);
	 	 clrscr;
	  end;
	  
	  if x = 3 then
	 	begin
	 	textbackground(lightblue);
	 	 clrscr;
	  end;
	  
	  if x = 4 then
	 	begin
	 	textbackground(yellow);
	 	 clrscr;
	  end;
	  
	  if x = 5 then
	 	begin
	 	textbackground(green);
	 	 clrscr;
	  end;
	  
	  if x = 6 then
	 	begin
	 	textbackground(cyan);
	 	 clrscr;
	  end;
	  
	  if x = 7 then
	 	begin
	 	textbackground(brown);
	 	 clrscr;  
	  end;
	  
		if x = 8 then
	 	begin
	 	textbackground(lightgreen);
	 	 clrscr;
	  end;
	  
	   if x = 9 then
	 	begin
	 	textbackground(8);
	 	 clrscr;  
	  end;
	  
		if x = 10 then
	 	begin
	 	textbackground(white);
	 	 clrscr;
	  end;
	  
	   if x = 11 then
	 	begin
	 	textbackground(7);
	 	 clrscr;  
	  end;
	  
		if x = 12 then
	 	begin
	 	textbackground(13);
	 	 clrscr;
	  end;
	  
	   if x = 13 then
	 	begin
	 	textbackground(5);
	 	 clrscr;  
	  end;
	  
		if x = 14 then
	 	begin
	 	textbackground(12);
	 	 clrscr;
	  end;
	 
	 
	end;
		textcolor(white);
		 if x = 0 then
		 write('A TELA FOI PRETA VOCE PERDEU TODOS OS PONTOS');
		 
	  textcolor(black);
	   if start = x then
	   	begin
	   	  case start of
	   	  	1:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI A AZUL');
	   	  		2:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI VERMELHO CLARO');
	   	  		3:                             
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI AZUL CLARO');
	   	  		4:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI AMARELO');
	   	  		5:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI VERDE');
	   	  		6:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI CIANO');
	   	  		7:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI MARROM');
	   	  		8:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI VERDE CLARO');
	   	  		9:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI CINZA ESCURO');
	   	  		10:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI BRANCA');
	   	  		11:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI CINZA CLARO');
	   	  		12:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI ROSA CLARO');
	   	  		13:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI ROSA ESCURO');
	   	  		14:
	   	  		writeln('VOCE ACERTOU!!!!! A COR FOI VERMELHO ESCURO');
	   	  end;
	   		
	   	end
	   	else
	   	write('ERROU ERROU FEIO ERROU RUDE');
		
	
	
		

    z:=z+1; 
 quit;
End.

