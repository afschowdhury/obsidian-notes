---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
pluginRouter.ts ^A6dqPMUs

routes/api/chatbot/pluginRouter/v4/ ^U5e1jv5l

- some authentication
- checks if it is a mesasge or
postback
- get stores data 
- send the data to main 
processor
- gets the output of the main 
processor and using reply
template , it creates an 
formatted reply  ^jY5RyXiU

using an aggregate function
full function in : src/controllers/store/storeChatbotController  ^TYgPlIRl

mainProcessor ^5rHa3TYU

src/chatbot/process/mainProcessor ^bkN2Uvh4

It creates a platform data from 
incoming data
- checks if further should go to 
nlp server or not
if so, then it sends the platform data 
to the nlp server( messageProcessor) ^v8uHJmYy

message processor 
 ^clBMdn15

- It will generate message answers form 
database queries with the help of messageActionProcessor ^8dFp2ZpL


# Embedded files
131b677cd3c804ea6c45f093d20d5387de9d0e07: [[Pasted Image 20230903103948_661.png]]
7a33198a35a50b9b75a1d8c8f86e9474c89a09a5: [[Pasted Image 20230903104207_715.png]]
91942682c178fc544c3796ee4ce1fbfedc20f489: [[Pasted Image 20230903105505_814.png]]

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/1.8.26",
	"elements": [
		{
			"id": "A6dqPMUs",
			"type": "text",
			"x": -305,
			"y": -207.84375,
			"width": 144.6998291015625,
			"height": 25,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 2028975229,
			"version": 31,
			"versionNonce": 1019643635,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716240813,
			"link": null,
			"locked": false,
			"text": "pluginRouter.ts",
			"rawText": "pluginRouter.ts",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 18,
			"containerId": null,
			"originalText": "pluginRouter.ts",
			"lineHeight": 1.25
		},
		{
			"id": "0co0dKLkcuH4F2JQPAHpB",
			"type": "rectangle",
			"x": -329,
			"y": -231.84375,
			"width": 195,
			"height": 79,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"seed": 1849221267,
			"version": 27,
			"versionNonce": 1040176573,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "mUaFxo-z3mq5HI2R7-NKB",
					"type": "arrow"
				}
			],
			"updated": 1693716240813,
			"link": null,
			"locked": false
		},
		{
			"id": "U5e1jv5l",
			"type": "text",
			"x": -431,
			"y": -323.84375,
			"width": 359.1395263671875,
			"height": 25,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1184589565,
			"version": 116,
			"versionNonce": 48181395,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "mUaFxo-z3mq5HI2R7-NKB",
					"type": "arrow"
				}
			],
			"updated": 1693716240813,
			"link": null,
			"locked": false,
			"text": "routes/api/chatbot/pluginRouter/v4/",
			"rawText": "routes/api/chatbot/pluginRouter/v4/",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 18,
			"containerId": null,
			"originalText": "routes/api/chatbot/pluginRouter/v4/",
			"lineHeight": 1.25
		},
		{
			"id": "mUaFxo-z3mq5HI2R7-NKB",
			"type": "arrow",
			"x": -250,
			"y": -285.84375,
			"width": 2,
			"height": 44,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 144491923,
			"version": 18,
			"versionNonce": 39327261,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716240813,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					2,
					44
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "U5e1jv5l",
				"focus": -0.0015052126153247073,
				"gap": 13
			},
			"endBinding": {
				"elementId": "0co0dKLkcuH4F2JQPAHpB",
				"focus": -0.14351110093842984,
				"gap": 10
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "jY5RyXiU",
			"type": "text",
			"x": -334,
			"y": -95.84375,
			"width": 312.359619140625,
			"height": 250,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 652366899,
			"version": 320,
			"versionNonce": 1917718675,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "0_FDw0l4GYq8eU55ohV1b",
					"type": "arrow"
				}
			],
			"updated": 1693716604409,
			"link": null,
			"locked": false,
			"text": "- some authentication\n- checks if it is a mesasge or\npostback\n- get stores data \n- send the data to main \nprocessor\n- gets the output of the main \nprocessor and using reply\ntemplate , it creates an \nformatted reply ",
			"rawText": "- some authentication\n- checks if it is a mesasge or\npostback\n- get stores data \n- send the data to main \nprocessor\n- gets the output of the main \nprocessor and using reply\ntemplate , it creates an \nformatted reply ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 243,
			"containerId": null,
			"originalText": "- some authentication\n- checks if it is a mesasge or\npostback\n- get stores data \n- send the data to main \nprocessor\n- gets the output of the main \nprocessor and using reply\ntemplate , it creates an \nformatted reply ",
			"lineHeight": 1.25
		},
		{
			"id": "-HQTZhuwmS4kInFmQU_Jr",
			"type": "image",
			"x": -1240.5,
			"y": -460.84375,
			"width": 687,
			"height": 366,
			"angle": 0,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1886224947,
			"version": 536,
			"versionNonce": 646531709,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "YITBmlwTXhe4qIgoFYuHD",
					"type": "arrow"
				}
			],
			"updated": 1693716240813,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "131b677cd3c804ea6c45f093d20d5387de9d0e07",
			"scale": [
				1,
				1
			]
		},
		{
			"id": "PX7NSsiIisLyL2PySMOnb",
			"type": "rectangle",
			"x": -354,
			"y": -121.84375,
			"width": 336,
			"height": 536,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"seed": 2001078451,
			"version": 111,
			"versionNonce": 726987485,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716240814,
			"link": null,
			"locked": false
		},
		{
			"id": "x5cmZvu4X3yGF3jNxaAM3",
			"type": "image",
			"x": -1263.5,
			"y": 38.32291666666663,
			"width": 809,
			"height": 53,
			"angle": 0,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1438890621,
			"version": 196,
			"versionNonce": 1577354803,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "_X0hpAUKrqjvqBV3cE8Zy",
					"type": "arrow"
				},
				{
					"id": "0_FDw0l4GYq8eU55ohV1b",
					"type": "arrow"
				}
			],
			"updated": 1693716604409,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "7a33198a35a50b9b75a1d8c8f86e9474c89a09a5",
			"scale": [
				1,
				1
			]
		},
		{
			"id": "YITBmlwTXhe4qIgoFYuHD",
			"type": "arrow",
			"x": -331,
			"y": -60.84375,
			"width": 221,
			"height": 100,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 1141399613,
			"version": 63,
			"versionNonce": 206533811,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716240814,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-221,
					-100
				]
			],
			"lastCommittedPoint": null,
			"startBinding": null,
			"endBinding": {
				"elementId": "-HQTZhuwmS4kInFmQU_Jr",
				"focus": -0.11555894268180178,
				"gap": 1.5
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "TYgPlIRl",
			"type": "text",
			"x": -1904.5833333333335,
			"y": 54.14583333333337,
			"width": 618.4192504882812,
			"height": 50,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1472647645,
			"version": 316,
			"versionNonce": 1546909789,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716412548,
			"link": null,
			"locked": false,
			"text": "using an aggregate function\nfull function in : src/controllers/store/storeChatbotController ",
			"rawText": "using an aggregate function\nfull function in : src/controllers/store/storeChatbotController ",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 43,
			"containerId": null,
			"originalText": "using an aggregate function\nfull function in : src/controllers/store/storeChatbotController ",
			"lineHeight": 1.25
		},
		{
			"id": "W8DDJjsuNA2b-Tkpb2GvH",
			"type": "ellipse",
			"x": -1936.9166666666665,
			"y": 0.47916666666674246,
			"width": 665.3333333333331,
			"height": 167.66666666666652,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 1927772925,
			"version": 185,
			"versionNonce": 1240185971,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "_X0hpAUKrqjvqBV3cE8Zy",
					"type": "arrow"
				}
			],
			"updated": 1693716409779,
			"link": null,
			"locked": false
		},
		{
			"id": "_X0hpAUKrqjvqBV3cE8Zy",
			"type": "arrow",
			"x": -1260.6731290207845,
			"y": 74.86440737757434,
			"width": 8.576870979215528,
			"height": 0.717971802061939,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 589663293,
			"version": 265,
			"versionNonce": 2029688829,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716426013,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-3.5768709792155278,
					-0.05190737757433794
				],
				[
					-8.576870979215528,
					0.6660644244876011
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "W8DDJjsuNA2b-Tkpb2GvH",
				"gap": 12.572165623340045,
				"focus": -0.1718909333475245
			},
			"endBinding": {
				"elementId": "x5cmZvu4X3yGF3jNxaAM3",
				"focus": 0.5698722867792151,
				"gap": 5.75
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "0_FDw0l4GYq8eU55ohV1b",
			"type": "arrow",
			"x": -347.37499999999864,
			"y": 39.96645021644974,
			"width": 102.5,
			"height": 23.75,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 763571443,
			"version": 35,
			"versionNonce": 768030237,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716604409,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-102.5,
					23.75
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "jY5RyXiU",
				"focus": 0.17666879037691935,
				"gap": 13.374999999998636
			},
			"endBinding": {
				"elementId": "x5cmZvu4X3yGF3jNxaAM3",
				"focus": 0.7792914491131756,
				"gap": 4.625000000001364
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"type": "text",
			"version": 84,
			"versionNonce": 995355795,
			"isDeleted": false,
			"id": "5rHa3TYU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 260.37500000000136,
			"y": -213.03354978355026,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 134.99984741210938,
			"height": 25,
			"seed": 2028975229,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1693716647588,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "mainProcessor",
			"rawText": "mainProcessor",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "mainProcessor",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"type": "rectangle",
			"version": 72,
			"versionNonce": 1127985693,
			"isDeleted": false,
			"id": "6q_VdLNyBDmn01hMTzGI1",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 231.37500000000136,
			"y": -242.03354978355026,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 195,
			"height": 79,
			"seed": 1849221267,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"id": "tritfOj6lY7OeoHI3NtJJ",
					"type": "arrow"
				}
			],
			"updated": 1693716676297,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 210,
			"versionNonce": 1512501693,
			"isDeleted": false,
			"id": "bkN2Uvh4",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 139.30523681640761,
			"y": -345.03354978355026,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 343.83966064453125,
			"height": 25,
			"seed": 1184589565,
			"groupIds": [],
			"roundness": null,
			"boundElements": [
				{
					"id": "tritfOj6lY7OeoHI3NtJJ",
					"type": "arrow"
				}
			],
			"updated": 1693716676297,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "src/chatbot/process/mainProcessor",
			"rawText": "src/chatbot/process/mainProcessor",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "src/chatbot/process/mainProcessor",
			"lineHeight": 1.25,
			"baseline": 18
		},
		{
			"id": "tritfOj6lY7OeoHI3NtJJ",
			"type": "arrow",
			"x": 306.37500000000136,
			"y": -316.28354978355026,
			"width": 3.75,
			"height": 67.5,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 743851325,
			"version": 25,
			"versionNonce": 1967641747,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716676297,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					3.75,
					67.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "bkN2Uvh4",
				"focus": 0.033327747222671365,
				"gap": 3.75
			},
			"endBinding": {
				"elementId": "6q_VdLNyBDmn01hMTzGI1",
				"focus": -0.1623014767344664,
				"gap": 6.75
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "v8uHJmYy",
			"type": "text",
			"x": 227.62500000000136,
			"y": -90.03354978355026,
			"width": 394.99951171875,
			"height": 150,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1157730013,
			"version": 246,
			"versionNonce": 997272189,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693717025581,
			"link": null,
			"locked": false,
			"text": "It creates a platform data from \nincoming data\n- checks if further should go to \nnlp server or not\nif so, then it sends the platform data \nto the nlp server( messageProcessor)",
			"rawText": "It creates a platform data from \nincoming data\n- checks if further should go to \nnlp server or not\nif so, then it sends the platform data \nto the nlp server( messageProcessor)",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 143,
			"containerId": null,
			"originalText": "It creates a platform data from \nincoming data\n- checks if further should go to \nnlp server or not\nif so, then it sends the platform data \nto the nlp server( messageProcessor)",
			"lineHeight": 1.25
		},
		{
			"id": "ZyzMQbg44FYPREGfhyBQY",
			"type": "image",
			"x": 690.0951612903239,
			"y": -183.15854978355026,
			"width": 622.5596774193549,
			"height": 586.25,
			"angle": 0,
			"strokeColor": "transparent",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 533268989,
			"version": 356,
			"versionNonce": 326032051,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "YUUWSyVJQoo96842rMviI",
					"type": "arrow"
				}
			],
			"updated": 1693716919464,
			"link": null,
			"locked": false,
			"status": "pending",
			"fileId": "91942682c178fc544c3796ee4ce1fbfedc20f489",
			"scale": [
				1,
				1
			]
		},
		{
			"id": "JDVx-dQ7SrU-M4-9wOg_p",
			"type": "rectangle",
			"x": 175.12500000000136,
			"y": -118.78354978355026,
			"width": 465,
			"height": 291.25,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"seed": 366569619,
			"version": 44,
			"versionNonce": 1468593427,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "YUUWSyVJQoo96842rMviI",
					"type": "arrow"
				}
			],
			"updated": 1693716919464,
			"link": null,
			"locked": false
		},
		{
			"id": "YUUWSyVJQoo96842rMviI",
			"type": "arrow",
			"x": 572.6250000000014,
			"y": -132.53354978355026,
			"width": 105,
			"height": 22.5,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 767055187,
			"version": 45,
			"versionNonce": 2038094237,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693716919464,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					105,
					-22.5
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "JDVx-dQ7SrU-M4-9wOg_p",
				"focus": -0.6345363179534035,
				"gap": 13.75
			},
			"endBinding": {
				"elementId": "ZyzMQbg44FYPREGfhyBQY",
				"focus": 0.9292638840484864,
				"gap": 12.470161290322494
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "clBMdn15",
			"type": "text",
			"x": 1608.8750000000014,
			"y": -316.28354978355026,
			"width": 191.53976440429688,
			"height": 50,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 406901469,
			"version": 34,
			"versionNonce": 894259507,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693717097836,
			"link": null,
			"locked": false,
			"text": "message processor \n",
			"rawText": "message processor \n",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 43,
			"containerId": null,
			"originalText": "message processor \n",
			"lineHeight": 1.25
		},
		{
			"id": "pbsZacVTT95AF7KF4BIah",
			"type": "rectangle",
			"x": 1548.8750000000014,
			"y": -370.03354978355026,
			"width": 290,
			"height": 122.5,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"seed": 1887172349,
			"version": 55,
			"versionNonce": 231853949,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693717097836,
			"link": null,
			"locked": false
		},
		{
			"id": "8dFp2ZpL",
			"type": "text",
			"x": 1536.3750000000014,
			"y": -140.03354978355026,
			"width": 656.25,
			"height": 48,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 21288925,
			"version": 127,
			"versionNonce": 352880563,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1693717183257,
			"link": null,
			"locked": false,
			"text": "- It will generate message answers form \ndatabase queries with the help of messageActionProcessor",
			"rawText": "- It will generate message answers form \ndatabase queries with the help of messageActionProcessor",
			"fontSize": 20,
			"fontFamily": 3,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 43,
			"containerId": null,
			"originalText": "- It will generate message answers form \ndatabase queries with the help of messageActionProcessor",
			"lineHeight": 1.2
		}
	],
	"appState": {
		"theme": "dark",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#000000",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "hachure",
		"currentItemStrokeWidth": 1,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 3,
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": -970.1250000000014,
		"scrollY": 687.9241747835503,
		"zoom": {
			"value": 0.8
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"colorPalette": {},
		"currentStrokeOptions": null,
		"previousGridSize": null
	},
	"files": {}
}
```
%%