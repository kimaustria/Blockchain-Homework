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

# Puppeth Install

4. Run puppeth on the command line

./puppeth

5. Create network

![Screenshot 3](https://user-images.githubusercontent.com/70985179/107175591-3a116d00-699b-11eb-8bcd-058220e8cc17.png)

6. Select the options as indicated to configure a new genesis with Clique (Proof of Authority) consensus alogorithm and fund your accounts using your MyCrypto wallet generated public key

![Screenshot 4](https://user-images.githubusercontent.com/70985179/107175813-c6bc2b00-699b-11eb-83e8-715bb5f9d936.png)

7. Export genesis to network folder created as .json

![Screenshot 5](https://user-images.githubusercontent.com/70985179/107175957-20245a00-699c-11eb-9a26-5e26af8165d2.png)

# Initialize nodes

8. Initalize both nodes created

./geth init kimblockchain.json --datadir HWnode1

./geth init kimblockchain.json --datadir HWnode2

![Screenshot 6](https://user-images.githubusercontent.com/70985179/107176191-afca0880-699c-11eb-9b30-03a831c3ca08.png)

9. Execute mining for first node

./geth.exe --datadir HWnode1/ --mine --minerthreads 1 --unlock '0xbe27BE1F280a747976f3777E144dB55237CF447C' --password HWnode1/password.txt --rpc --allow-insecure-unlock

![Screenshot 7](https://user-images.githubusercontent.com/70985179/107176307-fb7cb200-699c-11eb-8159-285466bad5ea.png)

10. Execute mining for second node

./geth --datadir node2 --port 30304 --rpc --bootnodes " enode://4ad8c4c613d94f6a17c03a4864a76efea1098aced9af77cc0af389f2f017b99d7c86ff8c812d0612e76f2be2845e86ca1bfe9f08f959a1fbb9972f167c3ff0ef@127.0.0.1:30303 “ --ipcdisable

![Screenshot 8](https://user-images.githubusercontent.com/70985179/107176392-439bd480-699d-11eb-91d7-f39bfd3ca497.png)

# MyCrypto

11. Set Up Custom Node

Open MyCrypto app > click "Add Custom Node" > fill in pop up with the network information data set within the genesis created

![Screenshot 9](https://user-images.githubusercontent.com/70985179/107176533-a68d6b80-699d-11eb-93ca-06a0c73f7070.png)

12. Ensure you have a Keystore wallet created and log into your wallet

Click on create new wallet > generate a wallet > generate a keystore file > create a password > once created and back at main screen click on Keystore file > login using password created

![Screenshot 10](https://user-images.githubusercontent.com/70985179/107176553-b5741e00-699d-11eb-8b89-59a0173502a7.png)

![Screenshot 11](https://user-images.githubusercontent.com/70985179/107176559-b6a54b00-699d-11eb-9499-5ad0f475053f.png)

![Screenshot 12](https://user-images.githubusercontent.com/70985179/107176634-ebb19d80-699d-11eb-8618-7fee29160d77.png)

13. Copy public key paste it into "To Address" to test network transfer with any set amount

![Screenshot 13](https://user-images.githubusercontent.com/70985179/107177051-e30d9700-699e-11eb-8437-9524c540080a.png)

