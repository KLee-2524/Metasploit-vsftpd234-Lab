# Introduction to Metasploit Remake
In my freshman year, I had the opportunity to lead a hands-on workshop for the Forensics and Security Technology Club (FAST) that explored the foundational concepts of penetration testing and the [Lockheed Martin Cyber Kill Chain model](https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html). These concepts were accompanied by a hands-on penetration testing lab that guided attendees through the process of a simple penetration test. In this workshop, attendees would have the opportunity to:

1. Use [Nmap](https://nmap.org/) on their [Kali Linux](https://www.kali.org/) virtual machines (VMs) to scan an intentionally vulnerable target [Metasploitable 2](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/) VM
2. Indentify the vulnerable service, vsftpd 2.3.4, running on port 21 of the target VM
3. Use The National Institute of Standards and Technology's ([NIST](https://www.nist.gov/)) National Vulnerablity Database ([NVD](https://nvd.nist.gov/)) to gather more information about the target's vulnerability
4. Leverage [The Metasploit Framework](https://www.metasploit.com/) to exploit [CVE-2011-2523](https://nvd.nist.gov/vuln/detail/CVE-2011-2523) to exploit the backdoor in the vsftpd 2.3.4 service and gain root access to the target

## Decreasing Barrier To Entry
I took steps to make my workshop more accessible to any students that were interested in particpating, such as:

1. Providing written instructions and accompanying YouTube tutorial videos to assist with installing Kali Linux and Metasploitable 2
2. Posting addtional marketing on the club's social media platforms to raise awareness and reiterate the importance of completing all pre-requisites prior to attending my workshop

Unfortunately, despite my efforts, many attendees did not arrive with the appropriate VMs installed. To address this challenge, I leveraged the cloud and infrastructure as code (IaC) skills that I have learned over the course of several classes and internships to create a Terraform IaC template that automatically deploys identical, standardized, and isolated cybersecurity lab environments in the cloud that attendees can easily access via RDP or SSH, which should be included on most if not all computers.

# Metasploit_vsftpd234_Lab
Automatically deploy up to 256 copies of a penetration testing workshop lab environment consisting of attacking Kali Linux EC2 instances and target Ubuntu EC2 instances running a vulnerable version of vsftpd 2.3.4. The orchestration of these cloud resources should be handled by Terraform with minimal manual configuration on the host's part. Please refer to the accompanying [Eboard documentation](https://docs.google.com/document/d/18bhQ8ys_vuvzN6DAWv2tGSjqvdMsI9td0NMyAPoQdCw/edit?usp=sharing) to view the full workshop preparation, execution, and close out procedures: 
<p align="center">
<img width="511" height="490" alt="Introduction to Metasploit" src="https://github.com/user-attachments/assets/e32676ec-263f-45cf-a87c-e6df07b1b474" />
</p>


