# Blockchain - MyCrypto

# Create Nodes

1. Create empty directory for your nodes

mkdir HWnode1 HWnode2

2. Use geth to get new accounts from nodes created

./geth account new --datadir HWnode1

./geth account new --datadir HWnode2

![Screenshot 1](https://user-images.githubusercontent.com/70985179/107174793-1e0ccc00-6999-11eb-8acf-a7d747c18a2a.png)

3. Save password and keys produced from nodes

echo 'HWnode1' > node1/password.txt

echo 'HWnode2' > node2/password.txt

echo 'be27BE1F280a747976f3777E144dB55237CF447C' >> accounts.txt

echo '05bf012D9F8b2903f18C9361ee5E40Bb2a1217e7' >> accounts.txt

![Screenshot 2](https://user-images.githubusercontent.com/70985179/107175190-2b768600-699a-11eb-9e22-a6b6640214b5.png)
