#BLOCKCHAIN.PY

*Simple HTTP responses using basic transactions & bundled transactions (Blocks) to simulate Blockchain protocols*

Written in Python used cURL for HTTP requests. 
(No permenant database will be created, so after server is quit data is lost. Data retention in progress)

To run: <command> `python blockchain.py`
(Will auto run on Port 5000)

To create a new transaction use: 

`curl -X POST -H "Content-Type: application/json" -d '{
 "sender": "d4ee26eee15148ee92c6cd394edd974e",
 "recipient": "recipient",
 "amount": 10
}' "http://localhost:5000/transactions/new"`


To create register a node to the network:

`curl -X POST -H "Content-Type: application/json" -d '{
 "nodes": "0.0.0.0:5001"
}' "http://localhost:5000/nodes/register"`
