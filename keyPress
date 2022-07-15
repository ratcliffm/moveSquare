// Maliah Ratcliff 
// 10/22/21

@3
D=A
@width
M=D
 
@SCREEN
D=A
@sqrpos
M=D

(LOOPCONDITION) 
@width
D=M 
@KEYLOOP 
D; JEQ

(LOOP)
@40
D=A
@height
M=D

@sqrpos
A=M 
D=0
D=!D
M=D

@width 
M=M-1

(INNERLOOP) 
@height 
D=M
@RESETSQR  
D; JEQ

@32
D=A 
@sqrpos
M=D+M 
@sqrpos
A=M 
D=0
D=!D
M=D

@height
M=M-1

@INNERLOOP 
M; JEQ

@RESETSQR 
0; JMP 

(RESETSQR)
@1279 
D=A
@sqrpos
M=M-D
@LOOPCONDITION
0; JMP

(KEYLOOP) 
@24576
D=M
@currentkey 
M=D

@68
D=A
@currentkey
D=D-M
@DOWNLOOP // d
D; JEQ

@83
D=A
@currentkey
D=D-M
@RIGHTLOOP // s
D; JEQ

@65
D=A
@currentkey
D=D-M
@LEFTLOOP // a
D; JEQ

@87
D=A
@currentkey
D=D-M
@UPLOOP // W
D; JEQ

@KEYLOOP 
0; JMP


(RIGHTLOOP) 
// make screen white
@SCREEN
M=0
@SCREEN
D=A
@i
M=D
(loopright)
@i
D=M
@24576
D=D-A
@nextright
D; JGE
D=0
@i
A=M
M=D
@i
M=M+1
@loopright
0;JMP

(nextright)
// move square pos to the right 
@1
D=A
@sqrpos
M=M+D

@3 
D=A
@width
M=D
@LOOPCONDITION
0; JMP


(LEFTLOOP)
// make screen white
@SCREEN
M=0
@SCREEN
D=A
@i
M=D
(loopleft)
@i
D=M
@24576
D=D-A

@nextleft
D; JGE

D=0
@i
A=M
M=D
@i
M=M+1
@loopleft
0;JMP

(nextleft)
// move square pos to the right 
@5
D=A
@sqrpos
M=M-D

@3 
D=A
@width
M=D
@LOOPCONDITION
0; JMP


(DOWNLOOP) 
@SCREEN
M=0
@SCREEN
D=A
@i
M=D
(loopdown)
@i
D=M
@24576
D=D-A

@nextdown
D; JGE

D=0
@i
A=M
M=D
@i
M=M+1
@loopdown
0;JMP

(nextdown)
@125
D=A
@sqrpos
M=M+D

@3 
D=A
@width
M=D
@LOOPCONDITION
0; JMP


(UPLOOP) 
@SCREEN
M=0
@SCREEN
D=A
@i
M=D
(loopup)
@i
D=M
@24576
D=D-A

@nextup
D; JGE

D=0
@i
A=M
M=D
@i
M=M+1
@loopup
0;JMP

(nextup)
@99
D=A
@sqrpos
M=M-D

@3 
D=A
@width
M=D
@LOOPCONDITION
0; JMP


(end) // infinite loop to end file - not likely needed since we have event loop for key 
@end
0; JMP 
