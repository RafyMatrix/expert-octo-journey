Program Timer ;  // By rafael's Duarte
var
 x,t0:integer;
 nova:char;

function timer(x,t0:integer):integer;
begin
 timer:=1+1;
 textcolor(blue);	
 writeln('digite o tempo do cronometro:');
 read(t0);
 for x:=t0 downto 0 do
 begin
 delay(1000);
 gotoxy(1,4);
 textcolor(green);
 write('Contagem Regressiva: ');
 gotoxy(21,4);
 textcolor(red);
 write( x:2:0);
end;

end;
Begin
while true do
	begin
	timer(x,t0);
	writeln('Nova Contagem? (s/n)');
	read(nova);
	if (nova = 's') or (nova ='S') then
	clrscr
	else
		break;
end;

   clrscr;
   write('Programa encerrado aperte <Enter para sair>');
   readkey;

   
End.
