[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/j-1-RQp-)
# CECS 378 Reading Assignment: Malware

### Assignment Description
Answer the following questions from the Chapter 6 reading from your text book. Be complete with your answers. You may work on these questions with one or two other partners, but *all* students must submit the document individually in their own repositories along with each student's name documented with the submission.

1. What mechanisms can a virus use to conceal itself?
    Viruses can hid themselves using several methods. These include stealth techniques that make infected files appear clean, encryption and polymorphism to change their code and avoid detection, rootkits to manipulate operaring system, and living off the land tactics to blend in with normal system behavior 
2. What is a *logic bomb*?
   A logic is a piece of malicious code that remains inactive unitel specific conditions are met once triggered it executes its  playload, which can couse damage like crashing he system ir deletinge files.

3. How does a Trojan enable malware to propagate? How common are Trojans on computer systems? Or on mobile platforms?
   Trojans spread by disguising themselves as legitmate software. When installed they allow maicious code to execute, downlading more malware or creating backdoors.Trojans are common on computer systems due to phishing and exploited vulnerabilities but are less common on mobile plataform. 

4. What is the difference between machine executable and macro viruses?
   Machine excutable viruses infect executable files caan affect operating system directly. Macro viruses, written in macro languages like VBA infect documents and spreadsheets and are spread through email attachments or shared files 

7. The following code fragments show a sequence of virus instructions and a metamorphic version of the virus.
 Describe the effect produced by the metamorphic code.
The methamophuc version introduces unnecessary instructions ( 'push' and pop ecx , swap eax, ebx and swap ebx , eax ) that do not change the overall behavior of the code and this make it dicicult for antivirus sortware to detect the vurus using matching techniques.

    ``` python
    #Original Code
        mov eax, 5 # invalid syntax 
        add eax, ebx
        call ebx
    
    #Metamorphic Code
        mov eax, 5
        push ecx
        pop ecx
        add eax, ebx
        swap eax, ebx
        swap ebx, eax
        call ebx
    ```

9. Consider the following fragment. What type of malware is this?
    
    ``` C
    [legitimate code]
    if data is Friday the 13th;
        crash_computer();
    [legitimate code] 
    ```
    This fragment is an example of a logic bomb it remains dormant unit a specific condition in this case the data bring friday the 13 is met at which point it executes its payload, which is to crash the computer 

10. Assume you have found a USB memory stick in your work parking area. What threats might this pose to your work computer should you just plug the memory stick in and examine its contents? In particular, consider whether each of the malware propagation mechanisms we discuss could use such a memory stick for transport. What steps could you take to mitigate these threats, and safely determine the contents of the memory stick?

11. Consider the following fragment in an authentication program. What type of malware is this?:

    ``` c
    username = read_username();
    password = read_password();
    if username is "133t h4ck0r"
	    return ALLOW_LOGIN;
    if username and password are valid
	    return ALLOW_LOGIN
    else return DENY_LOGIN
    ```
backdoor it allows unautherized access to the system bypassing the normal authentication proccess for a specifiv username 

12. Suppose you receive a letter from a finance company stating that your loan payments are in arrears (in default), and that action is required to correct this. However, as far as you know, you have never applied for, or received, a loan from this company! What may have occurred that led to this loan being created? What type of malware, and on which computer systems, might have provided the necessary information to an attacker that enabled them to successfully obtain this loan?
    The type malware is the indentity theft where an attacker may have stolen your personal and financial information such as name address and dat of birth

sythetic identity frauf the attacker migth have created a synthetic identity by combining real and fake information 
    
14. List the types of attacks on a personal computer that each of a (host-based) personal firewall, and anti-virus software, can help you protect against. Which of these counter-measures would help block the spread of macro viruses spread using email attachments? Which would block the use of backdoors on the system?
15. Personal firewall
    - unauthorized access attempts
    - port scans
    - denial of service  attacs
    - blocking suspicious traffic and preventing backdoors from commuocating with their command and control servers
    - alerting to suspicious activity

  Anti-virus software 
  -vruses 
  -Trojans 
  spyware 
  ransomware 
  macro viruses 
  detecting and removing malicious code from emial attachments, fukke and system memory 
### Deliverables

Commit the answers to the questions in a readable file to your git repository by the due date and time indicated with your repository on GitHub Classroom. The only approved file submission format is Markdown. Other formats will only be accepted with explicit approval.

#### Please note:

* Your writeup file *must* be done in [Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) format and must be included in the repository as a separate file. View the file [`README.md`](README.md?plain=1) for an example of Markdown.
* Any included images or screenshots should be done in `*.jpg`, `*.png`, or `*.gif` formats, and be included individually as files in your repository (i.e. no binary ‘document’ with the images pasted inside).
* Screenshots or images *may* be linked in your Markdown file writeup if you wish to do so.
