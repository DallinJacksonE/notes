
# Stack Notes

- The stack pointer can be manipulated to get values that appear later in your code to user values and then they will be reset as you run through the code

## Recursive Procedures

- a function that calls itself

- in assembly, it looks exactly the same, save registers, set up arguments, use call instruction, start executing code!

Ex:

```
long rsum(long n) {
	if (n == 0) {
		return 0;
	}
	else {
		return n + rsum(n-1);
	}
}
```
In assembly:
```
rsum:
pushq %rbx 		#Save rbx
irmovq $1, %r11
irmovq $0, %r10
rrmovq %rdi, %rbx	#store n
rrmovq %r10, %rax	#set return of 0
andq %rdi, %rdi		#set flags
je end
subq %r11, %rdi
call rsum
addq %rbx, %rax		#n+ rsum(n-1)
end:
popq %rbx 		#restoring rbx
ret			#return
```

