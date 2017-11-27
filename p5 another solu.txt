.586
.MODEL FLAT
INCLUDE io.h
.STACK 4096

.DATA
	 y BYTE "Enter Grade ",0
	 x BYTE "The Division of Grades is " , 0
	 z BYTE "The Reminder  " , 0
	 e1 SDWORD 11 , 0
	res SDWORD 11 DUP(?)

.CODE
	_MainProc PROC
	
	   input y , e1 , 11
	   atod e1
	   mov ebx , eax
  
       input y , e1 , 11
	   atod e1
	   add ebx , eax

	   input y , e1 , 11
	   atod e1
	   add ebx , eax

	   input y , e1 , 11
	   atod e1
	   add ebx , eax

	   mov edx , 0
	   mov eax , ebx

	   mov ecx , 4
	   div ecx
	  
	    
	  dtoa res , eax
	  output x , res

	  dtoa res , edx
	  output z , res
		mov eax , 0
		ret
	_MainProc ENDP

END