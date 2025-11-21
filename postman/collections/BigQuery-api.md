{
	"info": {
		"_postman_id": "50053765-45ce7dce-776c-435d-8267-5f937c0a8ca3",
		"name": "BigQuery API Documentation",
		"description": "## BigQuery API\n\nA data platform for customers to create, manage, and share query data.\n\n## Base URL\n\n[<code>bigquery.googleapis.com/bigquery/v1</code>](https://bigquery.googleapis.com/bigquery/v2)\n\n## Authorization\n\nAuthorization: Bearer {{access_token}}\n\nContent-Type: application/json\n\n### OAuth scopes (examples):\n\n- `https://www.googleapis.com/auth/bigquery`\n    \n- `https://www.googleapis.com/auth/cloud-platform`",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
	},
	"item": [
		{
			"name": "Get a list of datasets",
			"id": "50053765-1f8f8a0f-21fa-4de1-ba34-55a9d6121de3",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "ya29.c.c0ASRK0GaVMZOyji31ikDAmFgopBXf1c-F77tWv2TRQ81ouj3-NaxxiweBmR6YwRngeoM64QW-8UMF-T4-Z12CY6hpMOumW6o0yPWQa-VRqk2K4NlggAHJZxAEl5zYg6h_yhlycXxZ98Y6zw_GhUCHYgzXbKbgPznTXyuWEvJI8jcd8dGxVg-zMVZLLBZRi3HmVNMvy3Pmx8Bu0yZifRqpztpdX0-wNzYjGSl_LiVJwSTy2HNumVj24I3e6gb3_Qc2OPQmBNmgtpXTp03zh36AYOpMSli-FvsQ3GrcvawefThbg97GPQ20dGv6cCeFx2vLxymeqNCbzUDzHwEfn2qNbAof90un5SQ9AliargCzvxpIN_BgKqayFaFwnh2Cr8SfHUr7L397P3top_uUfn9vpVIJZ-li2_i0peplxQYjsjXk-Syjil-Qosr35bmhj0O6O0ne9R0gQ3VnYrvcRRcsX8mFxfJ2WXFplft40Yf0t-X7Sx_Y--Jowl59Ra3-a-BaxoJa9ZS2F4Oq1B4Mef58Zrya9pJQox2cFo-s2cm2XvZa88od_xu8Bw58Mz5Manpi31adBRJvzml3g9dZYYkvjZ4gV-clsQM0OR73Y2joZSgfRSZwkxn6o9gSocq-Wi7fSWU1rMZIzR21z-h7z1mb5sg8WJ_6RmcuvgSgSR0xgsQ-iIhSZWypgRn0Sd-1V-uqW0uoW2ifn4au55hcjJnS2s_ivubrnxcrIaXs2hO_amzZQWaYkymhp1Zz5V-YXJmS5h0-Vg81elQyhnUVFclb091yy0XiS-SVIjx2bXfhhQd80SIsgJQVva1uRRWYUbvfVu0va50r186hVxWI_9xZ_IitqQR4Ux4-5y4Y2usZpa3Z6yRm_R2icQhR2-02kwx_9nBSnbuim6hQY8xWQhs9j7n2wnBStmJaSMM5zRQW3u1iwdrsqlvdgIglUVQfc9MziiF6539k3999vauOp3OZpYwx9sh1M_J82fRF0sMYFghMowgU6vQ07jR",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [],
				"url": {
					"raw": "https://bigquery.googleapis.com/bigquery/v2/projects/bigquery-api-docs-001/datasets",
					"protocol": "https",
					"host": [
						"bigquery",
						"googleapis",
						"com"
					],
					"path": [
						"bigquery",
						"v2",
						"projects",
						"bigquery-api-docs-001",
						"datasets"
					]
				},
				"description": "## Get a list of datasets\n\n## **HTTP Request**\n\nGET\n\n### **Endpoint Path**\n\nGET /v1/projects/{projectId}/datasets\n\n**URL**: `/[https://bigquery.googleapis.com/bigquery/v2/projects/{{projectId}}/datasets]`  \nReplace `{{projectId}}` with your project ID (example: `bigquery-api-docs-001`).\n\n## Description\n\nLists all datasets in the specified project to which you have been granted the READER dataset role.\n\n## Authentication\n\nAuthorization: Bearer {{access_token}}\n\nContent-Type: application/json\n\nRequires the following OAuth scopes:\n\n- `https://www.googleapis.com/auth/bigquery`\n    \n- `https://www.googleapis.com/auth/cloud-platform`\n    \n\n## Path Parameters\n\n| Name | Type | Required | Description |\n| --- | --- | --- | --- |\n| ProjectId | string | Yes | Google Cloud Project ID (example: `bigquery-api-docs-001`). |\n\n## HTTP Status Codes\n\n**200 OK** - Request succeeded\n\nReturns a list of datasets.\n\n``` json\n{\n  \"datasets\": [\n    {\n      \"datasetReference\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\"\n      },\n      \"friendlyName\": \"string\",\n      \"id\": \"string\",\n      \"kind\": \"bigquery#dataset\",\n      \"labels\": {\n        \"additionalProp1\": \"string\",\n        \"additionalProp2\": \"string\",\n        \"additionalProp3\": \"string\"\n      },\n      \"location\": \"string\"\n    }\n  ],\n  \"etag\": \"string\",\n  \"kind\": \"bigquery#datasetList\",\n  \"nextPageToken\": \"string\"\n}\n\n ```\n\n## Error Responses\n\n| Code | Meaning | Fix |\n| --- | --- | --- |\n| 401 Unauthorized | Missing/expired/invalid token | Pass a valid Bearer token |\n| 403 Forbidden | Token lacks BigQuery permissions | Give SA/Account `/roles/bigquery.user` |\n| 404 Not Found | Invalid projectId or access denied | Check projectId or permissions |"
			},
			"response": []
		},
		{
			"name": "Create a new empty dataset",
			"id": "50053765-0c67a053-e325-4c9d-bf4f-b9b35c21cc62",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"auth": {
					"type": "noauth"
				},
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "https://bigquery.googleapis.com/bigquery/v2/projects/bigquery-api-docs-001/datasets",
					"protocol": "https",
					"host": [
						"bigquery",
						"googleapis",
						"com"
					],
					"path": [
						"bigquery",
						"v2",
						"projects",
						"bigquery-api-docs-001",
						"datasets"
					]
				},
				"description": "## Create a dataset\n\n## **HTTP Request**\n\nPOST\n\n### **Endpoint Path**\n\nPOST /v1/projects/{projectId}/datasets\n\n**URL**: `/[https://bigquery.googleapis.com/bigquery/v2/projects/{{projectId}}/datasets]`  \nReplace `{{projectId}}` with your project ID (example: `bigquery-api-docs-001`).\n\n## Description\n\nCreate a new empty dataset.\n\n## Authentication\n\nAuthorization: Bearer {{access_token}}\n\nContent-Type: application/json\n\nRequires the following OAuth scopes:\n\n- `https://www.googleapis.com/auth/bigquery`\n    \n- `https://www.googleapis.com/auth/cloud-platform`\n    \n\n## Path Parameters\n\n| Name | Type | Required | Description |\n| --- | --- | --- | --- |\n| ProjectId | string | Yes | Google Cloud Project ID related to the dataset you want to create. |\n\n## Request Body\n\n``` json\n{\n  \"access\": [\n    {\n      \"dataset\": {\n        \"dataset\": {\n          \"datasetId\": \"string\",\n          \"projectId\": \"string\"\n        },\n        \"targetTypes\": [\n          \"TARGET_TYPE_UNSPECIFIED\"\n        ]\n      },\n      \"domain\": \"string\",\n      \"groupByEmail\": \"string\",\n      \"iamMember\": \"string\",\n      \"role\": \"string\",\n      \"routine\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"routineId\": \"string\"\n      },\n      \"specialGroup\": \"string\",\n      \"userByEmail\": \"string\",\n      \"view\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"tableId\": \"string\"\n      }\n    }\n  ],\n  \"creationTime\": \"string\",\n  \"datasetReference\": {\n    \"datasetId\": \"string\",\n    \"projectId\": \"string\"\n  },\n  \"defaultCollation\": \"string\",\n  \"defaultEncryptionConfiguration\": {\n    \"kmsKeyName\": \"string\"\n  },\n  \"defaultPartitionExpirationMs\": \"string\",\n  \"defaultRoundingMode\": \"string\",\n  \"defaultTableExpirationMs\": \"string\",\n  \"description\": \"string\",\n  \"etag\": \"string\",\n  \"friendlyName\": \"string\",\n  \"id\": \"string\",\n  \"isCaseInsensitive\": true,\n  \"kind\": \"bigquery#dataset\",\n  \"labels\": {\n    \"additionalProp1\": \"string\",\n    \"additionalProp2\": \"string\",\n    \"additionalProp3\": \"string\"\n  },\n  \"lastModifiedTime\": \"string\",\n  \"location\": \"string\",\n  \"maxTimeTravelHours\": \"string\",\n  \"satisfiesPzs\": true,\n  \"selfLink\": \"string\",\n  \"storageBillingModel\": \"string\",\n  \"tags\": [\n    {\n      \"tagKey\": \"string\",\n      \"tagValue\": \"string\"\n    }\n  ]\n}\n\n ```\n\n### Fields\n\n| Field | Type | Required | Description |\n| --- | --- | --- | --- |\n| datasetReference.datasetId | string | Yes | Unique dataset name. |\n| datasetReference.projectId | string | Yes | Google Cloud Project ID. |\n\n### Example Request Body\n\n``` json\n{\n  \"datasetReference\": {\n    \"datasetId\": \"{{datasetId}}\",\n    \"projectId\": \"{{projectId}}\"\n  },\n  \"location\": \"{{location}}\"\n}\n\n ```\n\n## HTTP Status Code\n\n**200 OK** - Request succeeded\n\nReturns a list of datasets.\n\n``` json\n{\n  \"access\": [\n    {\n      \"dataset\": {\n        \"dataset\": {\n          \"datasetId\": \"string\",\n          \"projectId\": \"string\"\n        },\n        \"targetTypes\": [\n          \"TARGET_TYPE_UNSPECIFIED\"\n        ]\n      },\n      \"domain\": \"string\",\n      \"groupByEmail\": \"string\",\n      \"iamMember\": \"string\",\n      \"role\": \"string\",\n      \"routine\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"routineId\": \"string\"\n      },\n      \"specialGroup\": \"string\",\n      \"userByEmail\": \"string\",\n      \"view\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"tableId\": \"string\"\n      }\n    }\n  ],\n  \"creationTime\": \"string\",\n  \"datasetReference\": {\n    \"datasetId\": \"string\",\n    \"projectId\": \"string\"\n  },\n  \"defaultCollation\": \"string\",\n  \"defaultEncryptionConfiguration\": {\n    \"kmsKeyName\": \"string\"\n  },\n  \"defaultPartitionExpirationMs\": \"string\",\n  \"defaultRoundingMode\": \"string\",\n  \"defaultTableExpirationMs\": \"string\",\n  \"description\": \"string\",\n  \"etag\": \"string\",\n  \"friendlyName\": \"string\",\n  \"id\": \"string\",\n  \"isCaseInsensitive\": true,\n  \"kind\": \"bigquery#dataset\",\n  \"labels\": {\n    \"additionalProp1\": \"string\",\n    \"additionalProp2\": \"string\",\n    \"additionalProp3\": \"string\"\n  },\n  \"lastModifiedTime\": \"string\",\n  \"location\": \"string\",\n  \"maxTimeTravelHours\": \"string\",\n  \"satisfiesPzs\": true,\n  \"selfLink\": \"string\",\n  \"storageBillingModel\": \"string\",\n  \"tags\": [\n    {\n      \"tagKey\": \"string\",\n      \"tagValue\": \"string\"\n    }\n  ]\n}\n\n ```\n\n## Error Responses\n\n| Code | Meaning | Fix |\n| --- | --- | --- |\n| 400 Bad Request | Missing datasetId or invalid name | Use valid characters; length ≤ 1024 |\n| 401 Unauthorized | Missing/expired/invalid token | Use a valid Bearer token |\n| 403 Forbidden | Token lacks BigQuery permissions | Grant `roles/bigquery.admin` or `/roles/bigquery.user` |\n| 409 Conflict | Dataset already exists | Use a different datasetId |"
			},
			"response": []
		},
		{
			"name": "Delete a dataset",
			"id": "50053765-5a5b9470-38c2-4c3e-aef3-87e88a6a09f7",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"auth": {
					"type": "noauth"
				},
				"method": "DELETE",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": ""
				},
				"url": {
					"raw": "https://bigquery.googleapis.com/bigquery/v2/projects/bigquery-api-docs-001/datasets/test",
					"protocol": "https",
					"host": [
						"bigquery",
						"googleapis",
						"com"
					],
					"path": [
						"bigquery",
						"v2",
						"projects",
						"bigquery-api-docs-001",
						"datasets",
						"test"
					]
				},
				"description": "## Delete a dataset\n\n## **HTTP Request**\n\nDELETE\n\n### **Endpoint Path**\n\nDELETE /v1/projects/{projectId}/datasets/{datasetId}\n\n**URL**: `/[https://bigquery.googleapis.com/bigquery/v2/projects/{{projectId}}/datasets/{{datasetId}}]`  \nReplace `{{projectId}}` with your project ID (example: `bigquery-api-docs-001`).\n\nReplace `{{datasetId}}` with your dataset ID.\n\n## Description\n\nDelete a dataset specified in the datasetId value.\n\n## Authentication\n\nAuthorization: Bearer {{access_token}}\n\nContent-Type: application/json\n\nRequires the following OAuth scopes:\n\n- `https://www.googleapis.com/auth/bigquery`\n    \n- `https://www.googleapis.com/auth/cloud-platform`\n    \n\n## Path Parameters\n\n| Name | Type | Required | Description |\n| --- | --- | --- | --- |\n| `projectId` | string | Yes | ID of the Google Cloud Project related to the dataset you want to delete. |\n| `datasetId` | string | Yes | The name of the dataset you want to delete. |\n\n## Query Parameters\n\n| Name | Type | Required | Description |\n| --- | --- | --- | --- |\n| `deleteContents` | string | Optional | If 'true', deletes all tables inside the dataset before deleting the dataset. |\n\n## HTTP Status Code\n\n**204 OK** - Dataset deleted successfully"
			},
			"response": []
		},
		{
			"name": "Update the fields of a dataset",
			"id": "50053765-48152d16-922a-47c3-b8d7-b4fb4d5281ae",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"method": "PATCH",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "https://bigquery.googleapis.com/bigquery/v2/projects/bigquery-api-docs-001/datasets/test",
					"protocol": "https",
					"host": [
						"bigquery",
						"googleapis",
						"com"
					],
					"path": [
						"bigquery",
						"v2",
						"projects",
						"bigquery-api-docs-001",
						"datasets",
						"test"
					]
				},
				"description": "## Update the fields of a dataset\n\n## **HTTP Request**\n\nPATCH\n\n### **Endpoint Path**\n\nPATCH /v1/projects/{projectId}/datasets/{datasetId}\n\n**URL**: `/[https://bigquery.googleapis.com/bigquery/v2/projects/{{projectId}}/datasets{datasetId}}]`  \nReplace `{{projectId}}` with your project ID (example: `bigquery-api-docs-001`).\n\nReplace `{{datasetId}}` with your dataset ID.\n\n## Description\n\nUpdate the fields of an exisitng dataset using patch semantics.\n\n## Authentication\n\nAuthorization: Bearer {{access_token}}\n\nContent-Type: application/json\n\nRequires the following OAuth scopes:\n\n- `https://www.googleapis.com/auth/bigquery`\n    \n- `https://www.googleapis.com/auth/cloud-platform`\n    \n\n## Path Parameters\n\n| Name | Type | Required | Description |\n| --- | --- | --- | --- |\n| projectId | string | Yes | Google Cloud Project ID related to the dataset you want to create. |\n| datasetId | string | Yes | The dataset you want to update. |\n\n## Request Body\n\nInclude the fields you want to update.\n\n``` json\n{\n  \"access\": [\n    {\n      \"dataset\": {\n        \"dataset\": {\n          \"datasetId\": \"string\",\n          \"projectId\": \"string\"\n        },\n        \"targetTypes\": [\n          \"TARGET_TYPE_UNSPECIFIED\"\n        ]\n      },\n      \"domain\": \"string\",\n      \"groupByEmail\": \"string\",\n      \"iamMember\": \"string\",\n      \"role\": \"string\",\n      \"routine\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"routineId\": \"string\"\n      },\n      \"specialGroup\": \"string\",\n      \"userByEmail\": \"string\",\n      \"view\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"tableId\": \"string\"\n      }\n    }\n  ],\n  \"creationTime\": \"string\",\n  \"datasetReference\": {\n    \"datasetId\": \"string\",\n    \"projectId\": \"string\"\n  },\n  \"defaultCollation\": \"string\",\n  \"defaultEncryptionConfiguration\": {\n    \"kmsKeyName\": \"string\"\n  },\n  \"defaultPartitionExpirationMs\": \"string\",\n  \"defaultRoundingMode\": \"string\",\n  \"defaultTableExpirationMs\": \"string\",\n  \"description\": \"string\",\n  \"etag\": \"string\",\n  \"friendlyName\": \"string\",\n  \"id\": \"string\",\n  \"isCaseInsensitive\": true,\n  \"kind\": \"bigquery#dataset\",\n  \"labels\": {\n    \"additionalProp1\": \"string\",\n    \"additionalProp2\": \"string\",\n    \"additionalProp3\": \"string\"\n  },\n  \"lastModifiedTime\": \"string\",\n  \"location\": \"string\",\n  \"maxTimeTravelHours\": \"string\",\n  \"satisfiesPzs\": true,\n  \"selfLink\": \"string\",\n  \"storageBillingModel\": \"string\",\n  \"tags\": [\n    {\n      \"tagKey\": \"string\",\n      \"tagValue\": \"string\"\n    }\n  ]\n}\n\n ```\n\n## HTTP Status Code\n\n**200 OK** - Request succeeded\n\nReturns the updated dataset metadata.\n\n## Error Responses\n\n| Code | Meaning | Fix |\n| --- | --- | --- |\n| 400 Bad Request | Invalid field or value | Check request body fields |\n| 401 Unauthorized | Missing/expired/invalid token | Use a valid Bearer token |\n| 403 Forbidden | Token lacks BigQuery permissions | Grant `roles/bigquery.admin` or `/roles/bigquery.user` |\n| 409 Conflict | Dataset doesn't exist | Verify datasetId |"
			},
			"response": []
		},
		{
			"name": "Replace all fields of a dataset",
			"id": "50053765-15bf45ad-f60f-4ca0-a3c2-0e6f29ab04fd",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"method": "PUT",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "https://bigquery.googleapis.com/bigquery/v2/projects/bigquery-api-docs-001/datasets/test",
					"protocol": "https",
					"host": [
						"bigquery",
						"googleapis",
						"com"
					],
					"path": [
						"bigquery",
						"v2",
						"projects",
						"bigquery-api-docs-001",
						"datasets",
						"test"
					]
				},
				"description": "## Replace all fields of a dataset\n\n## **HTTP Request**\n\nPUT\n\n### **Endpoint Path**\n\nPUT /v1/projects/{projectId}/datasets/{datasetId}\n\n**URL**: `/[https://bigquery.googleapis.com/bigquery/v2/projects/{{projectId}}/datasets/{{datasetId}}]`  \nReplace `{{projectId}}` with your project ID (example: `bigquery-api-docs-001`).\n\nReplace `{{datasetId}}` with your dataset ID.\n\n## Description\n\nComplelely replace all the fields of an exisitng dataset.\n\n## Authentication\n\nAuthorization: Bearer {{access_token}}\n\nContent-Type: application/json\n\nRequires the following OAuth scopes:\n\n- `https://www.googleapis.com/auth/bigquery`\n    \n- `https://www.googleapis.com/auth/cloud-platform`\n    \n\n## Path Parameters\n\n| Name | Type | Required | Description |\n| --- | --- | --- | --- |\n| projectId | string | Yes | Google Cloud Project ID related to the dataset you want to create. |\n| datasetId | string | Yes | The dataset you want to update. |\n\n## Request Body\n\nInclude all the fields you want to include in the dataset. If a field is omitted, it is removed.\n\n``` json\n{\n  \"access\": [\n    {\n      \"dataset\": {\n        \"dataset\": {\n          \"datasetId\": \"string\",\n          \"projectId\": \"string\"\n        },\n        \"targetTypes\": [\n          \"TARGET_TYPE_UNSPECIFIED\"\n        ]\n      },\n      \"domain\": \"string\",\n      \"groupByEmail\": \"string\",\n      \"iamMember\": \"string\",\n      \"role\": \"string\",\n      \"routine\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"routineId\": \"string\"\n      },\n      \"specialGroup\": \"string\",\n      \"userByEmail\": \"string\",\n      \"view\": {\n        \"datasetId\": \"string\",\n        \"projectId\": \"string\",\n        \"tableId\": \"string\"\n      }\n    }\n  ],\n  \"creationTime\": \"string\",\n  \"datasetReference\": {\n    \"datasetId\": \"string\",\n    \"projectId\": \"string\"\n  },\n  \"defaultCollation\": \"string\",\n  \"defaultEncryptionConfiguration\": {\n    \"kmsKeyName\": \"string\"\n  },\n  \"defaultPartitionExpirationMs\": \"string\",\n  \"defaultRoundingMode\": \"string\",\n  \"defaultTableExpirationMs\": \"string\",\n  \"description\": \"string\",\n  \"etag\": \"string\",\n  \"friendlyName\": \"string\",\n  \"id\": \"string\",\n  \"isCaseInsensitive\": true,\n  \"kind\": \"bigquery#dataset\",\n  \"labels\": {\n    \"additionalProp1\": \"string\",\n    \"additionalProp2\": \"string\",\n    \"additionalProp3\": \"string\"\n  },\n  \"lastModifiedTime\": \"string\",\n  \"location\": \"string\",\n  \"maxTimeTravelHours\": \"string\",\n  \"satisfiesPzs\": true,\n  \"selfLink\": \"string\",\n  \"storageBillingModel\": \"string\",\n  \"tags\": [\n    {\n      \"tagKey\": \"string\",\n      \"tagValue\": \"string\"\n    }\n  ]\n}\n\n ```\n\n## HTTP Status Code\n\n**200 OK** - Request succeeded\n\nReturns the updated dataset metadata.\n\n## Error Responses\n\n| Code | Meaning | Fix |\n| --- | --- | --- |\n| 400 Bad Request | Invalid field or value | Check request body fields |\n| 401 Unauthorized | Missing/expired/invalid token | Use a valid Bearer token |\n| 403 Forbidden | Token lacks BigQuery permissions | Grant `roles/bigquery.admin` or `/roles/bigquery.user` |\n| 409 Conflict | Dataset doesn't exist | Verify `datasetId` |"
			},
			"response": []
		}
	],
	"auth": {
		"type": "bearer"
	},
	"event": [
		{
			"listen": "prerequest",
			"script": {
				"id": "53782e6b-4778-4e8a-902c-c325c530723b",
				"type": "text/javascript",
				"packages": {},
				"requests": {},
				"exec": [
					""
				]
			}
		},
		{
			"listen": "test",
			"script": {
				"id": "d441d03e-47b6-4c71-9732-bb034dab2d43",
				"type": "text/javascript",
				"packages": {},
				"requests": {},
				"exec": [
					""
				]
			}
		}
	]
}
