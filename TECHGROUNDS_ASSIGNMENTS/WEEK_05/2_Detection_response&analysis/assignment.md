# [2/ Detection,response & analysis]

So far, we’ve mostly looked at the prevention of attacks. While you want to prevent as many attacks as possible, some attacks will slip through your prevention systems. The most common method of getting malicious software (malware) into a network is through social engineering.

When getting hit with an attack, there are usually three steps to follow: Detection, response, and analysis.

Detecting an (attempted) attack is the first step to stopping it and to preventing future attempts. Tools like Wireshark can help analyse a network to detect anomalies. Intrusion detection systems (IDS) and intrusion prevention systems (IPS) are also used for this purpose.

The first thing to do in response to a detected attack is trying to contain the damage. Depending on the kind of attack, the way you do this might differ. After the attack is contained, you can try to figure out the root cause of the attack, so that you can stop it. Finally, you enter the recovery phase, where you try to get all systems back online and you take stock of the damage done.

It is vitally important to have a plan in place for how to respond when an attack happens.

In the analysis phase, you document what you learned and harden your systems so that such an attack cannot happen again. Sometimes this can be as simple as updating the OS on a server.

Response, and analysis are part of a disaster recovery plan. This plan is an important part of a bigger business continuity plan. When a disaster strikes and infrastructure goes offline, a business could be done for. There are many strategies when it comes to mitigating a disaster. From just having a cold backup, to a redundant site.

For these strategies it is always important to keep track of the following metrics: How much data is lost on incident (Recovery Point Objective; RPO), how long it takes to be back online (Recovery Time Objective; RTO), and cost.

## Key-terms

- Intrusion detection systems (IDS)
- Intrusion prevention systems (IPS)
- Hack response strategies.
- The concept of systems hardening.
- Different types of disaster recovery options.
- (Recovery Point Objective; RPO)
- (Recovery Time Objective; RTO)

## Assignment

 Exercise:

- A Company makes daily backups of their database. The database is automatically recovered when a failure happens using the most recent available backup. The recovery happens on a different physical machine than the original database, and the entire process takes about 15 minutes. What is the RPO of the database?
- An automatic failover to a backup web server has been configured for a website. Because the backup has to be powered on first and has to pull the newest version of the website from GitHub, the process takes about 8 minutes. What is the RTO of the website?

### Used sources

[Plaats hier de bronnen die je hebt gebruikt.]

### Encountered problems

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Result

  Exercise:

- A Company makes daily backups of their database. The database is automatically recovered when a failure happens using the most recent available backup. The recovery happens on a different physical machine than the original database, and the entire process takes about 15 minutes. What is the RPO of the database?
  
  - Given that the backups are made daily and the recovery process takes about 15 minutes, the potential data loss (RPO) would be approximately one day, minus the time taken for recovery:
    
    RPO ≈ 1 day - 15 minutes
    
    Therefore, the Recovery Point Objective (RPO) for the database in this scenario is approximately 1 day minus 15 minutes.

- An automatic failover to a backup web server has been configured for a website. Because the backup has to be powered on first and has to pull the newest version of the website from GitHub, the process takes about 8 minutes. What is the RTO of the website
  
  - In this scenario, the RTO is the time it takes to bring the backup web server online and make it fully operational after a failure.
    
    Given that the process of failover to the backup web server takes about 8 minutes, including the time required to power on the server and pull the newest version of the website from GitHub, the RTO would be approximately 8 minutes.
    
    Therefore, the Recovery Time Objective (RTO) for the website in this scenario is approximately 8 minutes. This means that the company aims to have the website fully operational within 8 minutes after a failure occurs.

   