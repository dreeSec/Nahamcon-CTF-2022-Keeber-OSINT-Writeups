# Challenges: Keeber
Category: **OSINT**  
Difficulty: **Medium**  
Authors: **matlac#2291, **  
Points: **---**  
Solves: **---**

## Keeber 1
Points: **---**  
Solves: **---**

Challenge Description: 
You have been applying to entry-level cybersecurity jobs focused on reconnaissance and open source intelligence (OSINT). Great news! You got an interview with a small cybersecurity company; the Keeber Security Group. Before interviewing, they want to test your skills through a series of challenges oriented around investigating the Keeber Security Group.

The first step in your investigation is to find more information about the company itself. All we know is that the company is named Keeber Security Group and they are a cybersecurity startup. To start, help us find the person who registered their domain. The flag is in regular format.

### Approach
Starting off we get this prompt that the Keeber Security Group about them wanting us to perform an investigation on them using our OSINT knowledge. We see that someone registered a domain, so step 1 should be finding this website. Not too hard after a quick google search for Keeber Security Group.
![dfddd81bfe2ca1a3336a9b474ce48121](https://user-images.githubusercontent.com/74334127/166117283-c5340afc-305c-465c-b2ec-39c4bc33233f.png)

We can use external websites to find out who registered the domain, such as [`whois.com`](https://www.whois.com).

<img src="https://user-images.githubusercontent.com/74334127/166116672-db875f99-f941-4bd1-b14f-b03eeb9c9abc.png" width=75% height=75%>

flag: `flag{ef67b2243b195eba43c7dc797b75d75b}`

## Keeber 2
Points: **---**  
Solves: **---**

Challenge Description: 
The Keeber Security Group is a new startup in its infant stages. The team is always changing and some people have left the company. The Keeber Security Group has been quick with changing their website to reflect these changes, but there must be some way to find ex-employees. Find an ex-employee through the group's website. The flag is in regular format.

### Approach
We can use external websites to find out who registered the domain, such as ‘whois.com’

I started off looking at the Github for this one, and found a contributor named `Tiffany Douglas` who wasn’t on the `team` section of the website. However, I couldn't find the flag there. I then pivoted to the [Wayback Machine](https://web.archive.org/web/20220419212259/https://keebersecuritygroup.com/team/)  and noticed a snapshot was taken prior to the competition starting.

![fc7db81a79f629225d300d9571b81bee](https://user-images.githubusercontent.com/74334127/166117044-c7a52e14-6828-48db-bd10-c179712bca0d.png)

Looking at this, we can find the flag under Tiffany's name in the team section.
![c5ff30eec6f06363b4af0f0cba508ad3](https://user-images.githubusercontent.com/74334127/166117077-b3087375-f645-4039-8957-37b96739adff.png)

flag: `flag{cddb59d78a6d50905340a62852e315c9}`

## Keeber 3
Points: **---**  
Solves: **---**
### Approach

