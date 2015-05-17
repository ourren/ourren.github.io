title: Nice paper on 23rd USENIX security
categories:
  - research
tags:
  - paper
  - security
date: 2015-01-25 20:32:30
---

Although the 24rd USENIX security symposium is calling for paper, but I have not saw any papers of 23rd USENIX security symposium. So I am plan to read some nice papers about my area and write some note every week. <!-- more -->

### paper list

I have picked some papers just from my interest as below:

1. Privee: An Architecture for Automatically Analyzing Web Privacy Policies	
	>Note: compare with common browser AD plugins, the paper desribe the automatic classification technology.
	
2. XRay: Enhancing the Web’s Transparency with Differential Correlation

	>Note: the idea is very nice, from the recommend result we can infer the facts which could affect the result. But the evaluation seems difficult for me to understand. 

3. An Internet-Wide View of Internet-Wide Scanning

	>Note: many aspects analysis: the type of scanner, the servive name, the ip address, the host providers, the research scanner, the vulnerable service scan, the reflect from organization and etc.. Really detail and fully consider. Did not have any algorithm.
	
4. Exit from Hell? Reducing the Impact of Amplification DDoS Attacks

5. Effective Attacks and Provable Defenses for Website Fingerprinting

6. A Bayesian Approach to Privacy Enforcement in Smartphones

7. The Long “Taile” of Typosquatting Domain Names

	>Note: talk about the long string domain with similar words(typosquatting). Also associate with the whois information. There domains are used for parking, malware, phishing, and etc..

8. Understanding the Dark Side of Domain Parking
	
	>Note: the paper are better than the previous paper. Because it have analyzed the whole aspect of parking domains. How the parking domain company could got profit from parking domains. But the expricence are last for several months, and author also bought some domains to dig the dark side of domain parking.

9. Towards Detecting Anomalous User Behavior in Online Social Networks

	>Principal Component Analysis (PCA) that models the behavior of normal users accurately and identifies significant deviations from it as anomalous. Our key insight, which we validate empirically, is that normal user be- havior in online social networks can be modeled using￼￼USENIX Association only a small number of suitably chosen latent features. Principal Component Analysis (PCA), a technique with well-known applications in uncovering network traffic anomalies [44], can be used to uncover anomalous be- havior. Such anomalous behavior may then be subjected to stricter requirements or manual investigations.
	
10. Man vs. Machine: Practical Adversarial Detection of Malicious Crowdsourcing Workers

11. Password Managers: Attacks and Defenses

	>the idea also appeard in my brain, but the author's thought have included all kinds of security issue about the password managers. Such as the domain and path, protocal, form action, autocomplete attribute and etc.
	
12. The Emperor’s New Password Manager: Security Analysis of Web-based Password Managers

	>compare to the above paper, this paper analyze more real security issues. But it only talked one popular password manager(lastpass, not keepass, 1pass). Maybe the other popular app did not have any vulnerability.
	
13. A Large-Scale Empirical Analysis of Chinese Web Passwords

	>Analyze the digital, characters, letter, keyboard patterns, pingyin, dates, and the structures of password, then put forward PCFG (Probabilistic Context-Free Grammar) based password guessing method by inserting Pinyins (about 2.3% more entries) into the attack dictionary and insert our observed composition rules into the guessing rule set.
	>very similar paper 2014 NDSS:[The Tangled Web of Password Reuse]

14. Automatically Detecting Vulnerable Websites Before They Turn Malicious

15. Hulk: Eliciting Malicious Behavior in Browser Extensions

16. Precise Client-side Protection against DOM-based Cross-Site Scripting

17. On the Effective Prevention of TLS Man-in-the-Middle Attacks in Web Applications