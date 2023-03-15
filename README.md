# Lab5_202001025
## Lab 5 - Static Analysis
### Code Lines having the error
def block_websites(start_hour, end_hour):
    while True:
        if (
            dt(dt.now().year, dt.now().month, dt.now().day, start_hour)
            < dt.now()
            < dt(dt.now().year, dt.now().month, dt.now().day, end_hour)
        ):
            print("Do the work ....")
            with open(default_hoster, "r+") as hostfile:
                hosts = hostfile.read()
                for site in sites_to_block:
                    if site not in hosts:
                        hostfile.write(redirect + " " + site + "\n")
        else:
            with open(default_hoster, "r+") as hostfile:
                hosts = hostfile.readlines()
                hostfile.seek(0)
                for host in hosts:
                    if not any(site in host for site in sites_to_block):
                        hostfile.write(host)
                hostfile.truncate()
            print("Good Time")
        time.sleep(3)
        
### Screenshot of Error found
![Screenshot 2023-03-15 150044](https://user-images.githubusercontent.com/122976431/225268454-af5a340f-6725-4e28-b4cc-3f2c80c2eab2.png)

### Github Repo: Website Blocker Python
Github Repo Link: https://github.com/Kalebu/Website-blocker-python
