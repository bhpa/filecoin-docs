### **lotus 节点API**

一、chian

1. ChainNotify返回带有链头更新的引用，第一条消息保证为len==1，type=='current'。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainNotify", "params": [], "id": 3}

返回：{

​    "jsonrpc": "2.0",

​    "result": {

​        "Cids": [

​            {

​                "/": "bafy2bzacednghy3w2e42xqrgeisswleti2uf2dno4ffaieuge2wfrbigqwdv6"

​            }

​        ],

​        "Blocks": [

​            {

​                "Miner": "t00",

​                "Ticket": {

​                    "VRFProof": "dnJmIHByb29mMDAwMDAwMHZyZiBwcm9vZjAwMDAwMDA="

​                },

​                "ElectionProof": {

​                    "VRFProof": ""

​                },

​                "BeaconEntries": [

​                    {

​                        "Round": 0,

​                        "Data": "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA="

​                    }

​                ],

​                "WinPoStProof": null,

​                "Parents": null,

​                "ParentWeight": "0",

​                "Height": 0,

​                "ParentStateRoot": {

​                    "/": "bafy2bzaceabkxvqaj6q6u2bq4nzmwkk7c4buzj76yoek3yxfptaia6hstuxik"

​                },

​                "ParentMessageReceipts": {

​                    "/": "bafy2bzaceaa43et73tgxsoh2xizd4mxhbrcfig4kqp25zfa5scdgkzppllyuu"

​                },

​                "Messages": {

​                    "/": "bafy2bzacecgw6dqj4bctnbnyqfujltkwu7xc7ttaaato4i5miroxr4bayhfea"

​                },

​                "BLSAggregate": null,

​                "Timestamp": 1592524800,

​                "BlockSig": null,

​                "ForkSignaling": 0

​            }

​        ],

​        "Height": 0

​    },

​    "id": 3

}

 

2. 返回当前链头

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainHead", "params": [], "id": 3}

 返回：

{
    "jsonrpc": "2.0",
    "result": {
        "Cids": [
            {
                "/": "bafy2bzaceczb5gpwzmfihank53ba43h4rjl23k5pcx7z43xdmo4p5fofh22qa"
            },
            {
                "/": "bafy2bzacedqopvxh452cn3quwua4qewpadmhlcciblpk653tsgni6grzatewi"
            }
        ],
        "Blocks": [
            {
                "Miner": "t02020",
                "Ticket": {
                    "VRFProof": "tBAnDLr5XJx7uxmwrq17NeesRdY+dgXxBlLN2pPyGAMTaC+UPw8xPjh5PQ5GKX5EDFKNAN4yZFp/fb73F6i3Pato34Q/yuoj/SZ7sAItpiL/JeSgVjIOOZFBEv4u+K0K"
                },
                "ElectionProof": {
                    "VRFProof": "obznWuJs20p9H/jpc9WiYdiHx8qzUusCJQ7mg1L8i8S4aj38i93vpcOO9eU1w3CpCPyEiArDNtOpDycWOyC/a/TxKPT6B6dcsI2sPqPfkVeI56aXErE86on0yohHiQ2P"
                },
                "BeaconEntries": [
                    {
                        "Round": 205553,
                        "Data": "gSneVmV85fYyZqj1ZFs1IAm/E9pz2BF17nllLx2zEMRFAEWxAm/hojE0tdypnZHGEvZvF5iZcfE7bmDGOv/MqL68pbS0cq/hLAmzLm9cBmIT5pBB3UsL8CeH6sirqxGC"
                    }
                ],
                "WinPoStProof": [
                    {
                        "PoStProof": 3,
                        "ProofBytes": "ssRkJlKHWssmh8abFvrN5x1rV3FQC9WAM2hYK2NNjDQEelUMx+CJ0P941uQylqCzkf7MQPJ0r3DjJgAPDOgPOBKsdPR4BXOurw1mY53Lx7xXpfwwROJqdea29tr3ktxHBZsArq3Sl5cCE43igpJsVcGhP6iD7Kb3L9w1gXcRkugnFgYoNZL3OEP5jLQY1z86opdTp1uwkr5eivEt+sqRSK+af7bC7GiQZ5Q61b2Vxs2+yuyd7+JsotDDdLwp5fXs"
                    }
                ],
                "Parents": [
                    {
                        "/": "bafy2bzacea24lcnctzolxc24k5utvvn33mgub4a3bfka7436jv32h3fviechg"
                    },
                    {
                        "/": "bafy2bzaceaeqajdqvcfjgroissn5jhwcsk6yyyo5gh5h34igt5kdbmdmpny24"
                    },
                    {
                        "/": "bafy2bzaceceld4xndb7tzrhmhoewlqhqstdjwtpfrenwpao7hzuhhf5s7hlzm"
                    },
                    {
                        "/": "bafy2bzacebatzr6572caj66bjnodkkntvszmwyudujjrgl75vxlbl2hofxctk"
                    },
                    {
                        "/": "bafy2bzaceb7roytvblia5jdl4g6z2jdoqzabqfepuef2speygklzrrba6evy2"
                    }
                ],
                "ParentWeight": "2095869309",
                "Height": 122369,
                "ParentStateRoot": {
                    "/": "bafy2bzacedcsprjo7ipsouwhesmuy76aqu4mq4kwedc3cvq22wekv3bbbzbgg"
                },
                "ParentMessageReceipts": {
                    "/": "bafy2bzacebadtki4dspp4edeuq4vekzfxvuohyhue6v2srovxxhxqfyp7gama"
                },
                "Messages": {
                    "/": "bafy2bzacea6jmp6dzwdabjb6mo2mu6irgxubsiinoyc5vbfhtivqtqsw4jc7i"
                },
                "BLSAggregate": {
                    "Type": 2,
                    "Data": "gkkY1vzxrXhhOL8PoGMhZ/9ZUuxXf0Q4zNey4PICHv89jDG4ylpGTUZ7WI/S+Yw6AvA5RCtzsqJ5cScF8JvkZhbpWjKMGhUKchZToR8sIYozlekY7QTSpPnMgRViDc+u"
                },
                "Timestamp": 1595584025,
                "BlockSig": {
                    "Type": 2,
                    "Data": "tfXovluNzXPsXJAr3CDWQtnXFTAJvSBjyyTZ2qghhBJxITKuDztqtCtmcFW2qq5VBsW7xAYNWZe3XmaXxtAo+10DC+TK0p45ZFzJYzd0+7mHwJZxS7pcu4nRERZCpgY8"
                },
                "ForkSignaling": 0
            },
            {
                "Miner": "t01025",
                "Ticket": {
                    "VRFProof": "kiKgR5Yzty19xVnJRH3KijKm6Puzsp0ShK1ZKiJzxZI1Z6rZoqitdiUiZ4Z9xmSWCPlWfw5LFOEx5GcBPEvxff1nTMxO1l0/Mfz8+qZ2cLRCv6XGCBQKsuUYI3u/Esac"
                },
                "ElectionProof": {
                    "VRFProof": "q+HGyokBxH7b3kv+VjfVPUJbA6OCBXsZ3Hbo0/yfjKVp3W1M/Xm5kki/C9wSr0yICzFEKoSXQrUDOkxFL5xKzY9doYDwJJX9/NSpDNQGs5g7bjwykdjdz+YIJm9J+X08"
                },
                "BeaconEntries": [
                    {
                        "Round": 205553,
                        "Data": "gSneVmV85fYyZqj1ZFs1IAm/E9pz2BF17nllLx2zEMRFAEWxAm/hojE0tdypnZHGEvZvF5iZcfE7bmDGOv/MqL68pbS0cq/hLAmzLm9cBmIT5pBB3UsL8CeH6sirqxGC"
                    }
                ],
                "WinPoStProof": [
                    {
                        "PoStProof": 3,
                        "ProofBytes": "ioNeFiUGuS52fHpowLovZGwn/DVjQDnTeheZAwDkw+L+FNov9EageJlwkI5kN8RMmKH+0uJgQQDi8MdoCrfxWcnd73aKxFQrlUmvFXHTlBtQPc1kaG1MDVbfpoXNFNnVC6n5MiH7+UFgvLMpNe06+xsIhCoouJwRDua67mZs0whl5vOermhVd65kiVKLHsCQhdJP/Bu+klrDA0iwGo64TD+p5psi8uxBASUqR6ffJ0YfBBAZYfoiiVHo7zrsaQ0N"
                    }
                ],
                "Parents": [
                    {
                        "/": "bafy2bzacea24lcnctzolxc24k5utvvn33mgub4a3bfka7436jv32h3fviechg"
                    },
                    {
                        "/": "bafy2bzaceaeqajdqvcfjgroissn5jhwcsk6yyyo5gh5h34igt5kdbmdmpny24"
                    },
                    {
                        "/": "bafy2bzaceceld4xndb7tzrhmhoewlqhqstdjwtpfrenwpao7hzuhhf5s7hlzm"
                    },
                    {
                        "/": "bafy2bzacebatzr6572caj66bjnodkkntvszmwyudujjrgl75vxlbl2hofxctk"
                    },
                    {
                        "/": "bafy2bzaceb7roytvblia5jdl4g6z2jdoqzabqfepuef2speygklzrrba6evy2"
                    }
                ],
                "ParentWeight": "2095869309",
                "Height": 122369,
                "ParentStateRoot": {
                    "/": "bafy2bzacedcsprjo7ipsouwhesmuy76aqu4mq4kwedc3cvq22wekv3bbbzbgg"
                },
                "ParentMessageReceipts": {
                    "/": "bafy2bzacebadtki4dspp4edeuq4vekzfxvuohyhue6v2srovxxhxqfyp7gama"
                },
                "Messages": {
                    "/": "bafy2bzacec7r25pykl6mv4emdfetuzqfy7nr6ktqtfkn3jfbsxep2s5m5zqpu"
                },
                "BLSAggregate": {
                    "Type": 2,
                    "Data": "pIa4n+boNM3ASENYFW6w8COwb+QG721i1E4Y26UY9Lv3s/8KAleTPEGAe0KLLzn1Ge3n694EUOzvtbDlUdkDdta4Em6RYHkwCdkuowneC6+qpzaWqPPFk64BeYQ8Zux/"
                },
                "Timestamp": 1595584025,
                "BlockSig": {
                    "Type": 2,
                    "Data": "kKXJ1TFhUvkEgu4d3O00GdzHYDKf1c+64R8SdLBt0OX7onJUj+Wd0LJBC7GK7bZDEV4JYJK4109i+Q+W58cK8H8LtPfQvWWG9FQMNufJn1nGw2K61PoUL+cIq4pSgR3Z"
                },
                "ForkSignaling": 0
            }
        ],
        "Height": 122369
    },
    "id": 3
}

3.ChainGetRandomness用于对链进行随机采样。

请求：{"jsonrpc":"2.0","method":"Filecoin.ChainGetRandomness","params": [tsk types.TipSetKey, personalization crypto.DomainSeparationTag, randEpoch abi.ChainEpoch, entropy []byte], "id": 3}

 

4.ChainGetBlock返回给定cid 对应的块。

请求：

{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetBlock", "params": [ {
                "/": "bafy2bzaceczb5gpwzmfihank53ba43h4rjl23k5pcx7z43xdmo4p5fofh22qa"
            }], "id": 3}

返回：

 {
    "jsonrpc": "2.0",
    "result": {
        "Miner": "t02020",
        "Ticket": {
            "VRFProof": "tBAnDLr5XJx7uxmwrq17NeesRdY+dgXxBlLN2pPyGAMTaC+UPw8xPjh5PQ5GKX5EDFKNAN4yZFp/fb73F6i3Pato34Q/yuoj/SZ7sAItpiL/JeSgVjIOOZFBEv4u+K0K"
        },
        "ElectionProof": {
            "VRFProof": "obznWuJs20p9H/jpc9WiYdiHx8qzUusCJQ7mg1L8i8S4aj38i93vpcOO9eU1w3CpCPyEiArDNtOpDycWOyC/a/TxKPT6B6dcsI2sPqPfkVeI56aXErE86on0yohHiQ2P"
        },
        "BeaconEntries": [
            {
                "Round": 205553,
                "Data": "gSneVmV85fYyZqj1ZFs1IAm/E9pz2BF17nllLx2zEMRFAEWxAm/hojE0tdypnZHGEvZvF5iZcfE7bmDGOv/MqL68pbS0cq/hLAmzLm9cBmIT5pBB3UsL8CeH6sirqxGC"
            }
        ],
        "WinPoStProof": [
            {
                "PoStProof": 3,
                "ProofBytes": "ssRkJlKHWssmh8abFvrN5x1rV3FQC9WAM2hYK2NNjDQEelUMx+CJ0P941uQylqCzkf7MQPJ0r3DjJgAPDOgPOBKsdPR4BXOurw1mY53Lx7xXpfwwROJqdea29tr3ktxHBZsArq3Sl5cCE43igpJsVcGhP6iD7Kb3L9w1gXcRkugnFgYoNZL3OEP5jLQY1z86opdTp1uwkr5eivEt+sqRSK+af7bC7GiQZ5Q61b2Vxs2+yuyd7+JsotDDdLwp5fXs"
            }
        ],
        "Parents": [
            {
                "/": "bafy2bzacea24lcnctzolxc24k5utvvn33mgub4a3bfka7436jv32h3fviechg"
            },
            {
                "/": "bafy2bzaceaeqajdqvcfjgroissn5jhwcsk6yyyo5gh5h34igt5kdbmdmpny24"
            },
            {
                "/": "bafy2bzaceceld4xndb7tzrhmhoewlqhqstdjwtpfrenwpao7hzuhhf5s7hlzm"
            },
            {
                "/": "bafy2bzacebatzr6572caj66bjnodkkntvszmwyudujjrgl75vxlbl2hofxctk"
            },
            {
                "/": "bafy2bzaceb7roytvblia5jdl4g6z2jdoqzabqfepuef2speygklzrrba6evy2"
            }
        ],
        "ParentWeight": "2095869309",
        "Height": 122369,
        "ParentStateRoot": {
            "/": "bafy2bzacedcsprjo7ipsouwhesmuy76aqu4mq4kwedc3cvq22wekv3bbbzbgg"
        },
        "ParentMessageReceipts": {
            "/": "bafy2bzacebadtki4dspp4edeuq4vekzfxvuohyhue6v2srovxxhxqfyp7gama"
        },
        "Messages": {
            "/": "bafy2bzacea6jmp6dzwdabjb6mo2mu6irgxubsiinoyc5vbfhtivqtqsw4jc7i"
        },
        "BLSAggregate": {
            "Type": 2,
            "Data": "gkkY1vzxrXhhOL8PoGMhZ/9ZUuxXf0Q4zNey4PICHv89jDG4ylpGTUZ7WI/S+Yw6AvA5RCtzsqJ5cScF8JvkZhbpWjKMGhUKchZToR8sIYozlekY7QTSpPnMgRViDc+u"
        },
        "Timestamp": 1595584025,
        "BlockSig": {
            "Type": 2,
            "Data": "tfXovluNzXPsXJAr3CDWQtnXFTAJvSBjyyTZ2qghhBJxITKuDztqtCtmcFW2qq5VBsW7xAYNWZe3XmaXxtAo+10DC+TK0p45ZFzJYzd0+7mHwJZxS7pcu4nRERZCpgY8"
        },
        "ForkSignaling": 0
    },
    "id": 3
}

5.ChainGetTipSet返回由给定的TipSetKey指定的tipset。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetTipSet", "params": [‘TipSetKey], "id": 3}

 

6. ChainGetBlockMessages 返回存储在指定区块的信息 

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetBlockMessages", "params": [ {
                "/": "bafy2bzaceczb5gpwzmfihank53ba43h4rjl23k5pcx7z43xdmo4p5fofh22qa"
            }], "id": 3}

返回： {
    "jsonrpc": "2.0",
    "result": {
        "BlsMessages": [
            {
                "Version": 0,
                "To": "t0118797",
                "From": "t3u7zjnzvigkpwokge5tu5jkvdtdlwlo2je4uub6uz6guj4vro2jp6ktzh2ksyft36hyjwwocbpca435p2defa",
                "Nonce": 35082,
                "Value": "0",
                "GasPrice": "1",
                "GasLimit": 1000000,
                "Method": 6,
                "Params": "hgMZH0zYKlgmAAFVwh8gU7yavPfBSHOsoVYQ3gg+YMlTJ4bvn7/xYofMs8ZFbEEaAAHQxoAaAJp7sw=="
            },
            {
                "Version": 0,
                "To": "t0118768",
                "From": "t3qyssqgkgqxa6ims36v3zsfutjhmj5zeljfob7nfsyhkq7ursmkjsdt3bkapbyrhetuobjfzknls2ianmeona",
                "Nonce": 166689,
                "Value": "0",
                "GasPrice": "1",
                "GasLimit": 1000000,
                "Method": 6,
                "Params": "hgMaAAHjmdgqWCYAAVXCHyAM8peDB92l2vgBOuEgc5P3fawHuWLilmCiOgnMdwK9LRoAAcqEgBoAmnwB"
            },
            {
                "Version": 0,
                "To": "t0118768",
                "From": "t3qyssqgkgqxa6ims36v3zsfutjhmj5zeljfob7nfsyhkq7ursmkjsdt3bkapbyrhetuobjfzknls2ianmeona",
                "Nonce": 166690,
                "Value": "0",
                "GasPrice": "1",
                "GasLimit": 1000000,
                "Method": 6,
                "Params": "hgMaAAHmS9gqWCYAAVXCHyBZIQSCV5fgZ9kqp9mwU+GjnjmlmtUg3iQMKNdSrKAHIBoAAdergBoAmnwB"
            }
        ],
        "SecpkMessages": [],
        "Cids": [
            {
                "/": "bafy2bzacedouholso62e55n2lgpg4zstjfiuo77w6pqd6hdftytofnpksfvmi"
            },
            {
                "/": "bafy2bzaceaez5hcfyvzftztatfqhqfuw2q3erltqfq3zhvdbj2riel5qhpw2m"
            },
            {
                "/": "bafy2bzaceanbzyuy2teswt7xnrjkowywwpduhfhgcaix6g64o5az6idvmhsfo"
            },
            {
                "/": "bafy2bzacecvcdcnv553r2zwlsgdsgnvhznxgqzwnlbuihlg5xwqbzecom6qwi"
            },
            {
                "/": "bafy2bzacea3olngazsmvlzfuscngx7p2glw2k2ldsex4conoovh6oeygra5pc"
            },
            {
                "/": "bafy2bzaceajuq3m2lxyskach73pxpy6baygntwn3dledaftgiscact2lgdupk"
            },
            {
                "/": "bafy2bzacedoobhoznm2r3uufi2cbka4dwuuhx26qwmpg2qtrr76fcpwekfmrw"
            },
            {
                "/": "bafy2bzacear67sq5pfdiqz223czfcg3wz2dxlc77bufeeiyt3vgur5m5jjtee"
            },
            {
                "/": "bafy2bzacebgpzsv3jqpz2ct5fgo5cxvcydzofkkcs45fgnykmwugienvi3uv6"
            },
            {
                "/": "bafy2bzacebeaxyiifekp5yndj5ylixzzszv2qtooti6u6m5ql6lxboxzxdzma"
            },
            {
                "/": "bafy2bzaceajl2wfmg6mmfl7yq3xmthi6adiaotftb2c6t4wzk7o6s4kvjpcge"
            },
            {
                "/": "bafy2bzacecqvugiek2n2udnnqcwmpcv5rgflaqogrcb3z47vicnqkyxl5cg42"
            },
            {
                "/": "bafy2bzacebn5kwfmoz66kfumvnecnvq7pnn6jbjx2skjlv2ludeta25ggv3ik"
            },
            {
                "/": "bafy2bzacebvmhiy6lpi6tibshjjrazug2iyarrcn4yn635osg7im2vto345wa"
            },
            {
                "/": "bafy2bzacedxxoqcddqevezwd5fqqva3mejj74rnl4ia34j7jhw3qmna7zxzou"
            },
            {
                "/": "bafy2bzacedoq7eofq3avlqalt23wa66nk2dzmoliuencrm6vjjrgawdfpklhm"
            },
            {
                "/": "bafy2bzacedzb3zfasae6kt776de2lw7zllobu4dqhlrj44iofeiztd5kt3z7c"
            },
            {
                "/": "bafy2bzacecqxyulmxzahiwl7arzvkpoexwmejdiqnoy6nfmvggs3cmqknish4"
            },
            {
                "/": "bafy2bzaceauqpj4qgefne2jbilndmmlfzh7z6aoamicqk5irfixbeal5aaruc"
            },
            {
                "/": "bafy2bzacecsrg3ndpxjyqgqpkf2eslteuqhcpl5xzjnrtzu5cd7afavflopvu"
            },
            {
                "/": "bafy2bzacea2ckhgrioa7oyaqbdr335wtfgrvyewfxjiwgb5hx2qujkfowevfy"
            },
            {
                "/": "bafy2bzaceai5q3u4u2t4vvfjnmdcwqzyh4caogx2hy4t5z6x67oxs462wcppm"
            },
            {
                "/": "bafy2bzacedt3bm7qr73hauxbxnailwbscbbxzgnh33q5vfqsqzsselvsnpd4c"
            },
            {
                "/": "bafy2bzacec4zoa7hcluevabmmv3ejxqqqpvpa3r37ap57smm5m24buoty6cum"
            },
            {
                "/": "bafy2bzaceauomocmd7e7ipt26vpzec3pqfidefowtlm4tzmut5pn5rm3p3hfq"
            }
        ]
    },
    "id": 3
}

7.ChainGetParentReceipts返回指定块的父提示集中消息的收据。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetParentReceipts", "params": [‘cid’], "id": 3}

 

8.ChainGetParentMessages返回存储在指定块的父提示集中的消息。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetParentMessages", "params": [‘cid’], "id": 3}

 

9.ChainGetTipSetByHeight在指定的epoch回过头来查找tipset。

//如果在指定的epoch没有块，则在较高的epoch处的tipset

//将被返回。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetTipSetByHeight", "params": [abi.ChainEpoch, types.TipSetKey], "id": 3}

 

10.ChainReadObj从chain读取指定CID引用的ipld节点并返回原始字节。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainReadObj", "params": [cid.Cid], "id": 3}

 

11.ChainHasObj检查链块存储中是否存在给定的CID。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainHasObj", "params": [cid.Cid,cid.Cid], "id": 3}

 

12.ChainSetHead强制设置当前链头。小心使用。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainSetHead", "params": [types.TipSetKey], "id": 3}

 

13.ChainGetGenesis返回genesis tipset。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetGenesis", "params": [], "id": 3}

 返回：

{
    "jsonrpc": "2.0",
    "result": {
        "Cids": [
            {
                "/": "bafy2bzacednghy3w2e42xqrgeisswleti2uf2dno4ffaieuge2wfrbigqwdv6"
            }
        ],
        "Blocks": [
            {
                "Miner": "t00",
                "Ticket": {
                    "VRFProof": "dnJmIHByb29mMDAwMDAwMHZyZiBwcm9vZjAwMDAwMDA="
                },
                "ElectionProof": {
                    "VRFProof": ""
                },
                "BeaconEntries": [
                    {
                        "Round": 0,
                        "Data": "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA="
                    }
                ],
                "WinPoStProof": null,
                "Parents": null,
                "ParentWeight": "0",
                "Height": 0,
                "ParentStateRoot": {
                    "/": "bafy2bzaceabkxvqaj6q6u2bq4nzmwkk7c4buzj76yoek3yxfptaia6hstuxik"
                },
                "ParentMessageReceipts": {
                    "/": "bafy2bzaceaa43et73tgxsoh2xizd4mxhbrcfig4kqp25zfa5scdgkzppllyuu"
                },
                "Messages": {
                    "/": "bafy2bzacecgw6dqj4bctnbnyqfujltkwu7xc7ttaaato4i5miroxr4bayhfea"
                },
                "BLSAggregate": null,
                "Timestamp": 1592524800,
                "BlockSig": null,
                "ForkSignaling": 0
            }
        ],
        "Height": 0
    },
    "id": 3
}

14.ChainTipSetWeight计算指定types.TipSetKey的权重

15.ChainGetNode计算指定types.TipSetKey的权重

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainTipSetWeight", "params": [types.TipSetKey], "id": 3}

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetNode", "params": [string], "id": 3}

 

16.ChainGetMessage从链区块库读取指定CID引用的消息。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetMessage", "params": [cid.Cid], "id": 3}

 

17.// ChainGetPath returns a set of revert/apply operations needed to get from

​    // one tipset to another, for example:

​    //```

​    //        to

​    //         ^

​    // from   tAA

​    //   ^     ^

​    // tBA    tAB

​    //  ^---*--^

​    //      ^

​    //     tRR

​    //```

​    // Would return `[revert(tBA), apply(tAB), apply(tAA)]`

//ChainGetPath返回从一个tipset到另一个tipset所需的一组revert/apply操作，例如：

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainGetPath", "params": [from types.TipSetKey,  to  types.TipSetKey], "id": 3}

 

18.ChainExport returns a stream of bytes with CAR dump of chain data.

//ChainExport返回一个字节流，其中包含链数据的CAR dump。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.ChainExport", "params": [types.TipSetKey], "id": 3}

 

**二、sync**

// MethodGroup: Sync

// The Sync method group contains methods for interacting with and

// observing the lotus sync service.

//Sync method组包含用于与lotussync服务交互和观察的方法。

 

1. SyncState returns the current status of the lotus sync system.

   //返回lotussync系统的当前状态。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.SyncState ", "params": [], "id": 3}

 

2.// SyncSubmitBlock can be used to submit a newly created block to the. network through this node

//SyncSubmitBlock可用于通过此节点向网络提交新创建的块

请求：{ "jsonrpc": "2.0", "method": "Filecoin.SyncSubmitBlock", "params": [blk *types.BlockMsg

], "id": 3}

 

3.// SyncMarkBad marks a blocks as bad, meaning that it won't ever by synced. Use with extreme caution.

//SycMcAdBad标记块是坏的，这意味着它永远不会同步。使用时要格外小心。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.SyncMarkBad", "params": [cid.Cid], "id": 3}

 

4.// SyncCheckBad checks if a block was marked as bad, and if it was, returns the reason.

//SyncCheckBad检查块是否标记为坏的，如果是，则返回原因。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.SyncCheckBad", "params": [cid.Cid], "id": 3}

 

5.// SyncIncomingBlocks returns a channel streaming incoming, potentially not yet synced block headers.

////SyncIncomingBlocks返回一个通道流传入，可能尚未同步的块头。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.SyncIncomingBlocks", "params": [cid.Cid], "id": 3}

 

**三、****Mpool**

// MethodGroup: Mpool

​    // The Mpool methods are for interacting with the message pool. The message pool

​    // manages all incoming and outgoing 'messages' going over the network.

 //Mpool方法用于与消息池交互。消息池管理所有通过网络传入和传出的“消息”。



1.MpoolPending returns pending mempool messages.

//MpoolPending返回挂起的mempool消息。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MpoolPending", "params": [types.TipSetKey

], "id": 3}

 

2.MpoolPush pushes a signed message to mempool

//MpoolPush将签名消息推送到mempool

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MpoolPush", "params": [*types.SignedMessage], "id": 3}

 

3.// MpoolPushMessage atomically assigns a nonce, signs, and pushes a message to mempool.

//MpoolPushMessage原子性地分配一个nonce、签名并将消息推送到mempool。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MpoolPushMessage", "params": [*types.Message], "id": 3}

 

4.// MpoolGetNonce gets next nonce for the specified sender.

// Note that this method may not be atomic. Use MpoolPushMessage instead.

//MpoolGetNonce获取指定发送方的下一个nonce。

//请注意，此方法可能不是原子的。请改用MpoolPushMessage。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MpoolGetNonce", "params": [address], "id": 3}

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MpoolSub", "params": [], "id": 3}

 

5.// MpoolEstimateGasPrice estimates what gas price should be used for a

// message to have high likelihood of inclusion in ‘nblocksincl’ epochs.

//mpoolestimategsprice估计一条消息应该使用什么样的gas价格，以使其很有可能被纳入“nblocksincl”时代。

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MpoolEstimateGasPrice", "params": [nblocksincl uint64, sender address.Address, gaslimit int64, tsk types.TipSetKey], "id": 3}

 

四、MethodGroup: Miner

请求：{"jsonrpc":"2.0","method":"Filecoin.MinerGetBaseInfo","params": [address.Address, abi.ChainEpoch, types.TipSetKey], "id": 3}

 

请求：{ "jsonrpc": "2.0", "method": "Filecoin.MinerCreateBlock", "params": [*BlockTemplate], "id": 3}

 

**五、****wallet**

1.// WalletNew creates a new address in the wallet with the given sigType.

   //WalletNew使用给定的sigType在电子钱包中创建一个新地址。

​    WalletNew(context.Context, crypto.SigType) (address.Address, error)

请求：{ "jsonrpc": "2.0", "method": "Filecoin.WalletNew ", "params": [crypto.SigType], "id": 3}

返回： 

  {
    "jsonrpc": "2.0",
    "result": "t122jxwayipdlgskgp7yhthq75h54xelfh2jymyja",
    "id": 3
}

2.// WalletHas indicates whether the given address is in the wallet.

//WalletHas表示给定地址是否在钱包中。

​    WalletHas(context.Context, address.Address) (bool, error)

请求：

{ "jsonrpc": "2.0", "method": "Filecoin.WalletHas", "params": ["t1h56cv4v6t7nzztbo6rzusthm6bhy3dvr5qeahsa"], "id": 3}

返回：

{
    "jsonrpc": "2.0",
    "result": true,
    "id": 3
}

   

3. // WalletList lists all the addresses in the wallet.

   //WalletList列出了钱包中的所有地址。

WalletList(context.Context) ([]address.Address, error)

请求：{ "jsonrpc": "2.0", "method": "Filecoin.WalletList ", "params": [], "id": 3}

 {
    "jsonrpc": "2.0",
    "result": [
        "t126xxiiulnkuossapqwtrqd7rax7zaufcosmzgtq",
        "t1zljwugrgdbdd2nlr66mspdl5dkpvjyt4pqatlxi"
    ],
    "id": 3
}

4. // WalletBalance returns the balance of the given address at the current head of the chain.

   //WalletBalance返回给定地址在当前链头的余额。

WalletBalance(context.Context, address.Address) (types.BigInt, error)

请求：{ "jsonrpc": "2.0", "method": "Filecoin.WalletBalance", "params": [address.Address], "id": 3}

 

5. // WalletSign signs the given bytes using the given address.

   //WalletSign使用给定地址对给定字节进行签名。

​    WalletSign(context.Context, address.Address, []byte) (*crypto.Signature, error)

 请求：{ "jsonrpc": "2.0", "method": "Filecoin.WalletSign", "params": [address.Address, []byte], "id": 3}

 

6. // WalletSignMessage signs the given message using the given address.

   //WalletSignMessage使用给定的地址对给定的消息进行签名。

​    WalletSignMessage(context.Context, address.Address, *types.Message) (*types.SignedMessage, error)

   请求：{ "jsonrpc": "2.0", "method": "Filecoin.WalletSignMessage", "params": [address.Address, *types.Message], "id": 3}

 

7. // WalletVerify takes an address, a signature, and some bytes, and indicates whether the signature is valid.

​    // The address does not have to be in the wallet.

//WalletVerify接受地址、签名和一些字节，并指示签名是否有效。

//地址不必在钱包中。

​    WalletVerify(context.Context, address.Address, []byte, *crypto.Signature) bool

请求：{"jsonrpc":"2.0","method":"Filecoin.WalletVerify","params": [address.Address, []byte, *crypto.Signature], "id": 3}

 

 8.// WalletDefaultAddress returns the address marked as default in the wallet.

//WalletDefaultAddress返回钱包中标记为默认的地址。

​    WalletDefaultAddress(context.Context) (address.Address, error)

   请求：{"jsonrpc":"2.0","method":"Filecoin.WalletDefaultAddress","params": [], "id": 3}

 

9. // WalletSetDefault marks the given address as as the default one.

   //WalletSetDefault将给定地址标记为默认地址。

​    WalletSetDefault(context.Context, address.Address) error

​    请求：{"jsonrpc":"2.0","method":"Filecoin.WalletSetDefault","params": [address.Address], "id": 3}

 

10.// WalletExport returns the private key of an address in the wallet.

//WalletExport返回钱包中某个地址的私钥。

​    WalletExport(context.Context, address.Address) (*types.KeyInfo, error)

   请求：{"jsonrpc":"2.0","method":"Filecoin.WalletExport","params": [address.Address], "id": 3}

 

11. // WalletImport receives a KeyInfo, which includes a private key, and imports it into the wallet.

    //WalletImport接收一个KeyInfo，其中包含一个私钥，并将其导入到wallet中。

​    WalletImport(context.Context, *types.KeyInfo) (address.Address, error)

   请求：{"jsonrpc":"2.0","method":"Filecoin.WalletImport","params": [*types.KeyInfo], "id": 3}

 

   12.// WalletDelete deletes an address from the wallet.

​	//WalletDelete从电子钱包中删除一个地址。

​    WalletDelete(context.Context, address.Address) error

请求：{"jsonrpc":"2.0","method":"Filecoin.WalletDelete","params": [address.Address], "id": 3}

 

**六、** **Other**

​    // MethodGroup: Client

​    // The Client methods all have to do with interacting with the storage and

​    // retrieval markets as a client

 	//客户端方法都与作为客户机的存储和检索市场的交互有关



​    1.// ClientImport imports file under the specified path into filestore.

//ClientImport将指定路径下的文件导入文件存储。

ClientImport(ctx context.Context, ref FileRef) (cid.Cid, error)

 

​    2.// ClientStartDeal proposes a deal with a miner.

//ClientStartDeal提议与矿工达成协议。

ClientStartDeal(ctx context.Context, params *StartDealParams) (*cid.Cid, error)

 

​    3.// ClientGetDealInfo returns the latest information about a given deal.

//ClientGetDealInfo返回有关给定交易的最新信息。

ClientGetDealInfo(context.Context, cid.Cid) (*DealInfo, error)

 

​    // ClientListDeals returns information about the deals made by the local client.

//ClientListDeals返回有关本地客户端所做交易的信息。

ClientListDeals(ctx context.Context) ([]DealInfo, error)

 

​    // ClientHasLocal indicates whether a certain CID is locally stored.

//ClientHasLocal表示某个CID是否在本地存储。

ClientHasLocal(ctx context.Context, root cid.Cid) (bool, error)

 

​    // ClientFindData identifies peers that have a certain file, and returns QueryOffers (one per peer).

//ClientFindData标识具有特定文件的对等方，并返回QueryOffers（每个对等方一个）。

ClientFindData(ctx context.Context, root cid.Cid) ([]QueryOffer, error)

 

​    // ClientMinerQueryOffer returns a QueryOffer for the specific miner and file.

//ClientMinerQueryOffer返回特定miner和文件的QueryOffer。

ClientMinerQueryOffer(ctx context.Context, root cid.Cid, miner address.Address) (QueryOffer, error)

 

​    // ClientRetrieve initiates the retrieval of a file, as specified in the order.

//ClientRetrieve启动文件的检索，按顺序指定。

ClientRetrieve(ctx context.Context, order RetrievalOrder, ref *FileRef) error

 

​    // ClientQueryAsk returns a signed StorageAsk from the specified miner.

//ClientQueryAsk从指定的miner返回签名的StorageAsk。

ClientQueryAsk(ctx context.Context, p peer.ID, miner address.Address) (*storagemarket.SignedStorageAsk, error)

 

​    // ClientCalcCommP calculates the CommP for a specified file, based on the sector size of the provided miner.

//ClientCalcCommP根据提供的miner的扇区大小计算指定文件的CommP。

ClientCalcCommP(ctx context.Context, inpath string, miner address.Address) (*CommPRet, error)

 

​    // ClientGenCar generates a CAR file for the specified file.

//ClientGenCar为指定的文件生成CAR文件。

​    ClientGenCar(ctx context.Context, ref FileRef, outpath string) error

 

​    // ClientUnimport removes references to the specified file from filestore

//ClientUnimport从文件存储中删除对指定文件的引用

​    //ClientUnimport(path string)

 

​    // ClientListImports lists imported files and their root CIDs

//ClientListImports列出导入的文件及其根cid

​    ClientListImports(ctx context.Context) ([]Import, error)

 

​    //ClientListAsks() []Ask

 

​    **八、****MethodGroup: State**

​    // The State methods are used to query, inspect, and interact with chain state.

​    // All methods take a TipSetKey as a parameter. The state looked up is the state at that tipset.

​    // A nil TipSetKey can be provided as a param, this will cause the heaviest tipset in the chain to be used.

//State方法用于查询、检查和与chain State交互。

//所有方法都以TipSetKey作为参数。查到的state就是那个tipsetkey。

//可以将nil TipSetKey作为param提供，这将导致链中最重的tipset将被使用。

 

​    // StateCall runs the given message and returns its result without any persisted changes.

//StateCall运行给定的消息并返回其结果，而不进行任何持久的更改。

StateCall(context.Context, *types.Message, types.TipSetKey) (*InvocResult, error)

 

​    // StateReplay returns the result of executing the indicated message, assuming it was executed in the indicated tipset.

//staterelay返回执行指定消息的结果，假设它是在指定的tipset中执行的。

StateReplay(context.Context, types.TipSetKey, cid.Cid) (*InvocResult, error)

 

​    // StateGetActor returns the indicated actor's nonce and balance.

//StateGetActor返回指定的actor的nonce和balance。

StateGetActor(ctx context.Context, actor address.Address, tsk types.TipSetKey) (*types.Actor, error)

 

​    // StateReadState returns the indicated actor's state.

//StateReadState返回指定参与者的状态。

StateReadState(ctx context.Context, actor address.Address, tsk types.TipSetKey) (*ActorState, error)

 

​    // StateListMessages looks back and returns all messages with a matching to or from address, stopping at the given height.

//StateListMessages回溯并返回所有与“收件人”或“发件人”地址匹配的消息，并在给定的高度停止。

​    StateListMessages(ctx context.Context, match *types.Message, tsk types.TipSetKey, toht abi.ChainEpoch) ([]cid.Cid, error)

 

​    // StateNetworkName returns the name of the network the node is synced to

//StateNetworkName返回节点同步到的网络的名称

StateNetworkName(context.Context) (dtypes.NetworkName, error)

 

​    // StateMinerSectors returns info about the given miner's sectors. If the filter bitfield is nil, all sectors are included.

​    // If the filterOut boolean is set to true, any sectors in the filter are excluded.

​    // If false, only those sectors in the filter are included.

////StateMinerSectors返回有关给定矿工部门的信息。如果过滤器位字段为零，则包括所有扇区。

//如果filterOut布尔值设置为true，则排除筛选器中的所有扇区。

//如果为false，则只包括过滤器中的那些扇区。

StateMinerSectors(context.Context, address.Address, *abi.BitField, bool, types.TipSetKey) ([]*ChainSectorInfo, error)

 

​    // StateMinerProvingSet returns info about those sectors that a given miner is actively proving.

//StateMinerProvingSet返回给定miner正在积极证明的那些扇区的信息。

StateMinerProvingSet(context.Context, address.Address, types.TipSetKey) ([]*ChainSectorInfo, error)

 

​    // StateMinerProvingDeadline calculates the deadline at some epoch for a proving period

​    // and returns the deadline-related calculations.

//StateMinerProvingDeadline计算某个纪元的证明期的截止日期，并返回与截止日期相关的计算结果。

StateMinerProvingDeadline(context.Context, address.Address, types.TipSetKey) (*miner.DeadlineInfo, error)

 

​    // StateMinerPower returns the power of the indicated miner

//StateMinerPower返回指定矿工的算力

StateMinerPower(context.Context, address.Address, types.TipSetKey) (*MinerPower, error)

 

​    // StateMinerInfo returns info about the indicated miner

//StateMinerInfo返回有关指定miner的信息

StateMinerInfo(context.Context, address.Address, types.TipSetKey) (MinerInfo, error)

 

​    // StateMinerDeadlines returns all the proving deadlines for the given miner

//stateminertimes返回给定miner的所有证明截止日期

StateMinerDeadlines(context.Context, address.Address, types.TipSetKey) (*miner.Deadlines, error)

 

​    // StateMinerFaults returns a bitfield indicating the faulty sectors of the given miner

//StateMinerFaults返回一个位域，指示给定miner的故障扇区

StateMinerFaults(context.Context, address.Address, types.TipSetKey) (*abi.BitField, error)

 

​    // StateAllMinerFaults returns all non-expired Faults that occur within lookback epochs of the given tipset

//StateAllMinerFaults返回在给定tipset的回望周期内发生的所有未过期的错误

StateAllMinerFaults(ctx context.Context, lookback abi.ChainEpoch, ts types.TipSetKey) ([]*Fault, error)

 

​    // StateMinerRecoveries returns a bitfield indicating the recovering sectors of the given miner

//stateminerecoveries返回一个位字段，指示给定miner的恢复扇区

StateMinerRecoveries(context.Context, address.Address, types.TipSetKey) (*abi.BitField, error)

 

​    // StateMinerInitialPledgeCollateral returns the initial pledge collateral for the specified miner's sector

//statemineInitialDegordeCallateral返回指定矿业部门的初始质押抵押品

StateMinerInitialPledgeCollateral(context.Context, address.Address, abi.SectorNumber, types.TipSetKey) (types.BigInt, error)

 

​    // StateMinerAvailableBalance returns the portion of a miner's balance that can be withdrawn or spent

//StateMinerAvailableBalance返回矿工余额中可以提取或使用的部分

StateMinerAvailableBalance(context.Context, address.Address, types.TipSetKey) (types.BigInt, error)

 

​    // StateSectorPreCommitInfo returns the PreCommit info for the specified miner's sector

//StateSectorPremitInfo返回指定矿工扇区的预提交信息

StateSectorPreCommitInfo(context.Context, address.Address, abi.SectorNumber, types.TipSetKey) (miner.SectorPreCommitOnChainInfo, error)

 

​    // StateSectorGetInfo returns the on-chain info for the specified miner's sector

//StateSectorGetInfo返回指定矿工扇区的链上信息

​    StateSectorGetInfo(context.Context, address.Address, abi.SectorNumber, types.TipSetKey) (*miner.SectorOnChainInfo, error)

StatePledgeCollateral(context.Context, types.TipSetKey) (types.BigInt, error)

 

 // StateSearchMsg searches for a message in the chain, and returns its receipt and the tipset where it was executed

//StateSearchMsg在链中搜索消息，并返回其收据和执行该消息的提示集

StateSearchMsg(context.Context, cid.Cid) (*MsgLookup, error)

 

​    // StateWaitMsg looks back in the chain for a message. If not found, it blocks until the

​    // message arrives on chain, and gets to the indicated confidence depth.

//StateWaitMsg在链中查找消息。如果没有找到，它将阻塞，直到消息到达链上，并达到指定的置信深度。

StateWaitMsg(ctx context.Context, cid cid.Cid, confidence uint64) (*MsgLookup, error)

 

​    // StateListMiners returns the addresses of every miner that has claimed power in the Power Actor

//StateListMiners返回每个在权力参与者中声称拥有权力的矿工的地址

StateListMiners(context.Context, types.TipSetKey) ([]address.Address, error)

 

​    // StateListActors returns the addresses of every actor in the state

//StateListActors返回状态中每个参与者的地址

StateListActors(context.Context, types.TipSetKey) ([]address.Address, error)

 

​    // StateMarketBalance looks up the Escrow and Locked balances of the given address in the Storage Market

//StateMarketBalance在存储市场中查找给定地址的托管和锁定余额

StateMarketBalance(context.Context, address.Address, types.TipSetKey) (MarketBalance, error)

 

​    // StateMarketParticipants returns the Escrow and Locked balances of every participant in the Storage Market

//StateMarketParticipants返回存储市场中每个参与者的托管和锁定余额

StateMarketParticipants(context.Context, types.TipSetKey) (map[string]MarketBalance, error)

 

​    // StateMarketDeals returns information about every deal in the Storage Market

//StateMarketDeals返回存储市场中每个交易的信息

StateMarketDeals(context.Context, types.TipSetKey) (map[string]MarketDeal, error)

 

​    // StateMarketStorageDeal returns information about the indicated deal

//StateMarketStorageDeal返回有关指定交易的信息

StateMarketStorageDeal(context.Context, abi.DealID, types.TipSetKey) (*MarketDeal, error)

 

​    // StateLookupID retrieves the ID address of the given address

//StateLookupID检索给定地址的ID地址

StateLookupID(context.Context, address.Address, types.TipSetKey) (address.Address, error)

 

​    // StateAccountKey returns the public key address of the given ID address

//StateAccountKey返回给定ID地址的公钥地址

StateAccountKey(context.Context, address.Address, types.TipSetKey) (address.Address, error)

 

​    // StateChangedActors returns all the actors whose states change between the two given state CIDs

​    // TODO: Should this take tipset keys instead?

//StateChangedActors返回其状态在两个给定状态cid之间变化的所有参与者

//TODO:是否应该改为使用tipset键？

StateChangedActors(context.Context, cid.Cid, cid.Cid) (map[string]types.Actor, error)

 

​    // StateGetReceipt returns the message receipt for the given message

//StateGetReceipt返回给定消息的消息回执

StateGetReceipt(context.Context, cid.Cid, types.TipSetKey) (*types.MessageReceipt, error)

 

​    // StateMinerSectorCount returns the number of sectors in a miner's sector set and proving set

//StateMinerSectorCount返回矿工的扇区集和证明集中的扇区数

StateMinerSectorCount(context.Context, address.Address, types.TipSetKey) (MinerSectors, error)

 

​    // StateCompute is a flexible command that applies the given messages on the given tipset.

​    // The messages are run as though the VM were at the provided height.

//StateCompute是一个灵活的命令，它将给定的消息应用于给定的tipset。

//消息的运行方式与虚拟机在提供的高度相同。

​    StateCompute(context.Context, abi.ChainEpoch, []*types.Message, types.TipSetKey) (*ComputeStateOutput, error)

 

​    **九、** **MethodGroup: Msig**

​    // The Msig methods are used to interact with multisig wallets on the

​    // filecoin network

 //Msig方法用于与filecoin网络上的multisig钱包交互



​    // MsigGetAvailableBalance returns the portion of a multisig's balance that can be withdrawn or spent

//MsigGetAvailableBalance返回multisig余额中可以提取或使用的部分

MsigGetAvailableBalance(context.Context, address.Address, types.TipSetKey) (types.BigInt, error)

 

​    // MsigCreate creates a multisig wallet

//MsigCreate创建一个multisig钱包

​    // It takes the following params: <required number of senders>, <approving addresses>, <unlock duration><initial balance>, <sender address of the create msg>, <gas price>

//它采用以下参数：<required number of senders>，<approving addresses>，<unlock duration>,<initial balance>, <sender address of the create msg>, <gas price>

MsigCreate(context.Context, int64, []address.Address, abi.ChainEpoch, types.BigInt, address.Address, types.BigInt) (cid.Cid, error)

 

​    // MsigPropose proposes a multisig message

//MsigPropose提出一个multisig消息

​    // It takes the following params: <multisig address>, <recipient address>, <value to transfer>,

​    // <sender address of the propose msg>, <method to call in the proposed message>, <params to include in the proposed message>

MsigPropose(context.Context, address.Address, address.Address, types.BigInt, address.Address, uint64, []byte) (cid.Cid, error)

 

​    // MsigApprove approves a previously-proposed multisig message

//MsigApprove批准先前提出的multisig消息

​    // It takes the following params: <multisig address>, <proposed message ID>, <proposer address>, <recipient address>, <value to transfer>,

​    // <sender address of the approve msg>, <method to call in the proposed message>, <params to include in the proposed message>

MsigApprove(context.Context, address.Address, uint64, address.Address, address.Address, types.BigInt, address.Address, uint64, []byte) (cid.Cid, error)

 

​    // MsigCancel cancels a previously-proposed multisig message

//MsigCancel取消先前建议的multisig消息

​    // It takes the following params: <multisig address>, <proposed message ID>, <recipient address>, <value to transfer>,

​    // <sender address of the cancel msg>, <method to call in the proposed message>, <params to include in the proposed message>

MsigCancel(context.Context, address.Address, uint64, address.Address, types.BigInt, address.Address, uint64, []byte) (cid.Cid, error)

 

​    // MsigSwapPropose proposes swapping 2 signers in the multisig

//MsigSwapPropose建议在multisig中交换2个签名者

​    // It takes the following params: <multisig address>, <sender address of the propose msg>,

​    // <old signer> <new signer>

MsigSwapPropose(context.Context, address.Address, address.Address, address.Address, address.Address) (cid.Cid, error)

 

​    // MsigSwapApprove approves a previously proposed SwapSigner

//MsigSwapApprove批准先前提议的SwapSigner

​    // It takes the following params: <multisig address>, <sender address of the approve msg>, <proposed message ID>,

​    // <proposer address>, <old signer> <new signer>

MsigSwapApprove(context.Context, address.Address, address.Address, uint64, address.Address, address.Address, address.Address) (cid.Cid, error)

 

​    // MsigSwapCancel cancels a previously proposed SwapSigner message

//MsigSwapCancel取消先前建议的SwapSigner消息

​    // It takes the following params: <multisig address>, <sender address of the cancel msg>, <proposed message ID>,

​    // <old signer> <new signer>

​    MsigSwapCancel(context.Context, address.Address, address.Address, uint64, address.Address, address.Address) (cid.Cid, error)

 

​    MarketEnsureAvailable(context.Context, address.Address, address.Address, types.BigInt) (cid.Cid, error)

​    // MarketFreeBalance

 

   **十、** **MethodGroup: Paych**

​    // The Paych methods are for interacting with and managing payment channels

 //Paych方法用于与支付渠道进行交互和管理

PaychGet(ctx context.Context, from, to address.Address, ensureFunds types.BigInt) (*ChannelInfo, error)

 

PaychList(context.Context) ([]address.Address, error)

 

PaychStatus(context.Context, address.Address) (*PaychStatus, error)

 

PaychClose(context.Context, address.Address) (cid.Cid, error)

 

PaychAllocateLane(ctx context.Context, ch address.Address) (uint64, error)

 

PaychNewPayment(ctx context.Context, from, to address.Address, vouchers []VoucherSpec) (*PaymentInfo, error)

 

PaychVoucherCheckValid(context.Context, address.Address, *paych.SignedVoucher) error

 

PaychVoucherCheckSpendable(context.Context, address.Address, *paych.SignedVoucher, []byte, []byte) (bool, error)

 

PaychVoucherCreate(context.Context, address.Address, types.BigInt, uint64) (*paych.SignedVoucher, error)

 

PaychVoucherAdd(context.Context, address.Address, *paych.SignedVoucher, []byte, types.BigInt) (types.BigInt, error)

 

PaychVoucherList(context.Context, address.Address) ([]*paych.SignedVoucher, error)

 

PaychVoucherSubmit(context.Context, address.Address, *paych.SignedVoucher) (cid.Cid, error)

 