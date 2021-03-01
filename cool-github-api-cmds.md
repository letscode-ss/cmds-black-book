# github API commands
 
# Get list of repos fron org
```
curl -u <username>:<password> https://github.com/api/v3/orgs/<orgname>/repos?per_page=100 |jq -r " .[].name"
```

# create a repo

```
repoName="repo01"
curl -u <username>:<password> https://github.com/api/v3/orgs/<orgname>/repos -d '{"name":"'${repoName}'","private":"true", "visibility":"private"}'
``` 
 
# mirror repo
```
git clone ${sourceUrl} --bare
mirrorAuthUrl=`echo ${destGheUrl}/${destOrgName}/${repo}| sed -e "s|https://|https://${USER}:${TOKEN}@|g"`
git push --mirror ${mirrorAuthUrl};
```
