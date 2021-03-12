### 								**节点钱包API 及硬件钱包开发参考**

**一、钱包API**

1.**WalletNew**：在节点钱包中创建一个新地址。

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.WalletNew",
	"params": [1],
	"id": 3
}
```

参数 ：  1  表示 secp256k1 类型地址 

返回：
```json
{
	"jsonrpc": "2.0",
	"result": "t122jxwayipdlgskgp7yhthq75h54xelfh2jymyja",
	"id": 3
}
```

2.**WalletHas**：判断给定地址是否在钱包中。

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.WalletHas",
	"params": ["t1h56cv4v6t7nzztbo6rzusthm6bhy3dvr5qeahsa"],
	"id": 3
}
```

返回：
```json
{
	"jsonrpc": "2.0",
	"result": true,
	"id": 3
}
```
3.**WalletList**：列出了钱包中的所有地址。

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.WalletList",
	"params": [],
	"id": 3
}
```
返回：
```json
{
	"jsonrpc": "2.0",
	"result": ["t126xxiiulnkuossapqwtrqd7rax7zaufcosmzgtq", "t1zljwugrgdbdd2nlr66mspdl5dkpvjyt4pqatlxi"],
	"id": 3
}
```

4.**WalletBalance**：返回给定地址在当前链头的余额。

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.WalletBalance",
	"params": ["t3q5bnpkdrd72g3qge6dqibi2jvwukmnoeri3g7n4oc7urvyktswsoajb35nrtmeotdk2rfb2vudubmwhezb4q"],
	"id": 3
}
```
返回：
```json
{
	"jsonrpc": "2.0",
	"result": "49899499999825884666346257",
	"id": 3
}
```
返回说明：返回余额不带精度

5.**WalletExport**：导出钱包中某个地址的私钥。

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.WalletExport",
	"params": ["t3q5bnpkdrd72g3qge6dqibi2jvwukmnoeri3g7n4oc7urvyktswsoajb35nrtmeotdk2rfb2vudubmwhezb4q"],
	"id": 3
}
```
返回：
```json
{
	"jsonrpc": "2.0",
	"result": {
		"Type": "bls",
		"PrivateKey": "kyNMi2G+l8yz/zf/PNavmUdJrRVPaPQKvxXo6DUZRxQ="
	},
	"id": 3
}
```
返回说明： 
```
Type  -- 地址类型
PrivateKey -- 私钥
```


6.**WalletImport**：接收一个KeyInfo，其中包含一个私钥，并将其导入到wallet中。

请求：
```json

{
	"jsonrpc": "2.0",
	"method": "Filecoin.WalletImport",
	"params": [{
		"Type": "secp256k1",
		"PrivateKey": "W7p3zzG1hogoEsAnAYNqZdgGfkKg/GiNizrBY/KzcNs="
	}],
	"id": 3
}
```


返回：
```json
{
	"jsonrpc": "2.0",
	"result": "t13ocsxf2p4wchtbjpauft3wnebkp5uqrjmyov5aa",
	"id": 3
}
```
7.**ChainHead**:获取本地当前高度信息

请求：
```json
{
	"method": "Filecoin.ChainHead",
	"id": 3,
	"jsonrpc": "2.0",
	"params": []
}
```


返回：
```json
{
	"jsonrpc": "2.0",
	"result": {
		"Cids": [{
			"/": "bafy2bzaceckrmbsnmyeryewewfdspm2d67gt33tamoikdmiwntmee2cqiuqsm"
		}],
		"Blocks": [{
			"Miner": "t01000",
			"Ticket": {
				"VRFProof": "t9QdwqkPCHBjPS6GBgWvQQPAMn4px7m6XOJOCalkqSzwebjvradd6hShBDj1pOLaDzn3wA90tWVAwYimL92V6uoue/KVfNpoYbElUKjIojGnIbwmDjtcs5Epni7iICWR"
			},
			"ElectionProof": {
				"WinCount": 7,
				"VRFProof": "gUy9vMrpfueg+icE7a7/RdK3HFFBBO1O7Sae+FwW/Tgs9DMGexd4pP1Zg53JNxf5C4rL7xCFspIK7XsKLePrCxzayaTTdiAKnWtA2sEv36aOweWp3HhboyeDScp0p/vq"
			},
			"BeaconEntries": null,
			"WinPoStProof": [{
				"PoStProof": 0,
				"ProofBytes": "hzL3UETDMDg4ss50PFygg5K3zZF2/CH75nLASjuHdeoPZRBWGUdCcx1tAPoA0afqkVQJvYOXKplXsVMCG6ANA8M5/30FXujjHA15yFb3uRnHnb1diQHVZ9UwV6rH2RRfAVTHP+dM6OUzzcNz+g+rY2aghI67L/4f5J1ECtRo+a39Pxu04bXe36jyjk+TbwnUoNMRLnqC42/TkE6TQz6uxVPqJwN9Bk4SJhm+EGJ4e5506d8QTYIyxyg5ITINSPs7"
			}],
			"Parents": [{
				"/": "bafy2bzacedud4ecrzuy24x6guhtvvcr2rlwe7ghoxbuybuhg2zkougzdqioxo"
			}],
			"ParentWeight": "357318528",
			"Height": 62282,
			"ParentStateRoot": {
				"/": "bafy2bzaceajqo7fibugev3socd6bgm66t6g35vmr5t6qp6gjezczlgoknrjmm"
			},
			"ParentMessageReceipts": {
				"/": "bafy2bzacedswlcz5ddgqnyo3sak3jmhmkxashisnlpq6ujgyhe4mlobzpnhs6"
			},
			"Messages": {
				"/": "bafy2bzacecmda75ovposbdateg7eyhwij65zklgyijgcjwynlklmqazpwlhba"
			},
			"BLSAggregate": {
				"Type": 2,
				"Data": "wAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
			},
			"Timestamp": 1613967174,
			"BlockSig": {
				"Type": 2,
				"Data": "tFEuzzjYlu40we5vI0RrPQJG2eKwQJMOvtl0SlMhVXZT+FBTCwnpFhC8R62JbmQHEPPG0HUAO+RNbhW5n+s6cOQP7X7OahvTj3IqlV0WU5oNT3myzfmbhQ6sH+8GG6fY"
			},
			"ForkSignaling": 0,
			"ParentBaseFee": "100"
		}],
		"Height": 62282
	},
	"id": 3
}
```
返回说明：
```
Height -- 当前区块高度
Cids -- 当前高度cid 集合
```



8.**GasEstimateFeeCap**:获取当前预估GasFeeCap

```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.GasEstimateFeeCap",
	"params": [
		{
			"Version": 42,
			"To": "f01234",
			"From": "f01234",
			"Nonce": 42,
			"Value": "0",
			"GasLimit": 0,
			"GasFeeCap": "0",
			"GasPremium": "0",
			"Method": 1,
			"Params": "Ynl0ZSBhcnJheQ==",
			"CID": {
				"/": "bafy2bzacebbpdegvr3i4cosewthysg5xkxpqfn2wfcz6mv2hmoktwbdxkax4s"
			}
		},
		9,
		[
			{
				"/": "bafy2bzaceckrmbsnmyeryewewfdspm2d67gt33tamoikdmiwntmee2cqiuqsm"
			}
		]
	],
	"id": 3
}
```


返回：
```json
{
	"jsonrpc": "2.0",
	"result": "288",
	"id": 3
}
```
9.**GasEstimateGasLimit**:返回当前预估gasLimit

```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.GasEstimateGasLimit",
	"params": [
		{
			"Version": 42,
			"To": "f01234",
			"From": "f01234",
			"Nonce": 42,
			"Value": "0",
			"GasLimit": 0,
			"GasFeeCap": "0",
			"GasPremium": "0",
			"Method": 1,
			"Params": "Ynl0ZSBhcnJheQ==",
			"CID": {
				"/": "bafy2bzacebbpdegvr3i4cosewthysg5xkxpqfn2wfcz6mv2hmoktwbdxkax4s"
			}
		},
		[
			{
				"/": "bafy2bzaceckrmbsnmyeryewewfdspm2d67gt33tamoikdmiwntmee2cqiuqsm"
			}
		]
	],
	"id": 3
}
```


10. **GasEstimateGasPremium**:获取当前预估GasPremium

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.GasEstimateGasPremium",
	"params": [
		42,
		"f01234",
		9,
		[
			{
				"/": "bafy2bzacea3wsdh6y3a36tb3skempjoxqpuyompjbmfeyf34fi3uy6uue42v4"
			},
			{
				"/": "bafy2bzacebp3shtrn43k7g3unredz7fxn4gj533d3o43tqn2p2ipxxhrvchve"
			}
		]
	],
	"id": 3
}
```


返回:
```json
{
	"jsonrpc": "2.0",
	"result": "100420",
	"id": 3
}
```

11.**MpoolPush**:广播交易

请求：
```json
{
	"jsonrpc": "2.0",
	"method": "Filecoin.MpoolPush",
	"params": [
		{
			"Message": {
				"Version": 42,
				"To": "f01234",
				"From": "f01234",
				"Nonce": 42,
				"Value": "0",
				"GasLimit": 9,
				"GasFeeCap": "0",
				"GasPremium": "0",
				"Method": 1,
				"Params": "Ynl0ZSBhcnJheQ==",
				"CID": {
					"/": "bafy2bzacebbpdegvr3i4cosewthysg5xkxpqfn2wfcz6mv2hmoktwbdxkax4s"
				}
			},
			"Signature": {
				"Type": 2,
				"Data": "Ynl0ZSBhcnJheQ=="
			},
			"CID": {
				"/": "bafy2bzacebbpdegvr3i4cosewthysg5xkxpqfn2wfcz6mv2hmoktwbdxkax4s"
			}
		}
	],
	"id": 3
}
```


返回：
```json
{
	"jsonrpc": "2.0",
	"result": "{ " / ": "bafy2bzacea3wsdh6y3a36tb3skempjoxqpuyompjbmfeyf34fi3uy6uue42v4"}",
	"id": 3
}
```



**二、硬件钱包开发参考**

第三方钱包开发参考： https://github.com/Zondax/ledger-filecoin

硬件钱包客户端开发参考：https://github.com/whyrusleeping/ledger-filecoin-go

