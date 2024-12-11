# Email Analysis CTF Challenge 2

<h2>Description</h2>
In this email analysis challenge 2, I am a SOC Analyst at Global LOgistics and I've been tasked to investigate a user's password reset email for dropbox to see if it's legitimate or not. 


<h2>Languages and Utilities Used</h2>

- <b>https://github.com/MalwareCube/Email-IOC-Extractor</b>
- <b>Virustotal</b>


<h2>Environments Used </h2>

- <b>Unbuntu</b> 

<br />
<br />
Challenge 2 prompt.

![1) challenge prompt](https://github.com/user-attachments/assets/80fe9820-d770-43ff-9d8b-69fce61c4a07)

<br />
<br />
I used ioc python script from malwarecube to enumerate email sample headers.

![2) basic header enumeration](https://github.com/user-attachments/assets/44d16017-0e7f-4f5a-8736-6c4e1581273a)

<br />
<br />  
I used whois.domaintools to find the resolve host for ip 40.107.22.60.

![3) ASN and resolved hostname](https://github.com/user-attachments/assets/72b9463e-9124-49cc-8571-48bacb0b36be)

<br />
<br />
I used nslookup on the email.dropbox.com doamin to see the full spf record.

![4) email message ID and full spf record](https://github.com/user-attachments/assets/d4264320-38da-4308-b26a-ba3ce1f16c8a)

<br />
<br />
Uploading the email sample as file and extracting from quted printable, urls, and defang urls, I was able to enumerate the URL in the email. 

![5) defang cyberchef url](https://github.com/user-attachments/assets/19cc9f1b-b5fc-4e8b-b93a-e1a769002fff)

<br />
<br />
Uploading the fanged email url into talosintelligence shows a favorable reb reputation. All these artifacts along with the user's background situation leads me to conclude that this password reset is legitimate. 

![6) cisco talos genuine](https://github.com/user-attachments/assets/66a2fb72-cfe6-4dc3-afa0-9dc039498339)

<br />
<br />
