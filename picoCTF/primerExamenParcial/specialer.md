# Specialer

# Description
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.
Additional details will be available after launching your challenge instance.
# Solution
-  At first connection it looks like the most common commands don't work  but some commands still working like echo using the tab key I can see a list of the available commands and using echo * I can use it like an ls command

``` bash
# Avaliable commands 
Specialer$ 
!          compgen    exit       local      test
./         complete   export     logout     then
:          compopt    false      mapfile    time
LS         continue   fc         popd       times
[          coproc     fg         printf     trap
[[         declare    fi         pushd      true
]]         dirs       for        pwd        type
alias      disown     function   read       typeset
bash       do         getopts    readarray  ulimit
bg         done       hash       readonly   umask
bind       echo       help       return     unalias
break      elif       history    select     unset
builtin    else       if         set        until
caller     enable     in         shift      wait
case       esac       jobs       shopt      while
cd         eval       kill       source     {
command    exec       let        suspend    }
Specialer$ cd 
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd abra/    
Specialer$ echo *
cadabra.txt cadaniel.txt

```

- Due the availability of the ```mapfile``` command I can use it for read the contents of the text and see its contents with ```echo``` I did this in some directories until I finally found the flag.

```bash
 cd abra/    
Specialer$ echo *
cadabra.txt cadaniel.txt
Specialer$ cd cada
cadabra.txt   cadaniel.txt  
Specialer$ cd cada
cadabra.txt   cadaniel.txt  
Specialer$ cd cada
cadabra.txt   cadaniel.txt  
Specialer$ cd     
Specialer$ cd 
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd 
.hushlogin  .profile    abra/       ala/        sim/        
Specialer$ cd ala/
kazam.txt  mode.txt   
Specialer$ cd         
.hushlogin  .profile    abra/       ala/        sim/
Specialer$ cd abra/cada
cadabra.txt   cadaniel.txt  
Specialer$ cd abra/cada
cadabra.txt   cadaniel.txt  
Specialer$ cd abra/    
Specialer$ pwd
/home/ctf-player/abra
Specialer$ mapfile -t lineas < cadabra.txt
Specialer$ echo $lineas
Nothing up my sleeve!
Specialer$ mapfile -t lineas < cadaniel.txt
Specialer$ echo $lineas
Yes, I did it! I really did it! I'm a true wizard!
Specialer$ cd
Specialer$ cd ala/
Specialer$ echo *
kazam.txt mode.txt
Specialer$ mapfile -t lineas < kazam.txt
Specialer$ echo $lineas
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_838b49d1}
```

