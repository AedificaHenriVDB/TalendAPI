---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "SAP_EXTRACT_TEST"
    version: "1.0.0"
    description: "No description"
    contact: {}
  contract:
    baseUrls:
    - url: "https://2ig912ru1eka29u.eu.api-mocks.com"
      description: "This is your API mock endpoint. When called, it will simulate the behavior of your API."
      isPublished: true
    - url: "http://www.agilos.com"
      description: "Agilos"
      isPublished: true
    unsortedElementOrder:
    - "#/contract/resources/8cee4f24-d8cf-4302-93c9-53558f700cfa"
    - "#/contract/types/470db667-d635-4208-803d-db908e61d301"
    - "#/contract/types/05c5b5be-66b3-40c8-9f4c-75d9327d5566"
    - "#/contract/resources/e31499c4-a4ad-4878-8fc7-656b220a6f52"
    - "#/contract/resources/ea87eef0-bdfa-452e-9ae4-58c852158dc5"
    resources:
      "8cee4f24-d8cf-4302-93c9-53558f700cfa":
        path: "/Customer"
        operations:
          ac8c3ab8-f37f-4089-bed3-b4295a30c7cb:
            name: "Add Customer"
            method: "POST"
            bodies:
            - type: "#/contract/types/470db667-d635-4208-803d-db908e61d301"
              examples:
              - value: |-
                  {"ID": "1920",
                  "NAME": "Sofiene",
                  "LAST NAME": "Khayati",
                  "MAIL": "Sofiene.Khayati@agilos.com",
                  "PHONE": "0465784646",
                  "STREET_NUMBER": "12",
                  "CITY": "Ixelles",
                  "DEPARTMENT": "Brussels",
                  "REGION": "Brussels",
                  "COUNTRY": "Belgium",
                  "POSTAL_CODE": "1050"}
              mediaTypes:
              - "application/json"
            responses:
              "843c9cb3-4da1-4098-830a-04aee9501215":
                status: "200"
                description: "Customer Added"
      e31499c4-a4ad-4878-8fc7-656b220a6f52:
        path: "/Z_POH"
        operations:
          a6b9e8da-e3be-4472-b4f3-03be430a009b:
            name: "SAP_Z_POH"
            method: "GET"
            description: "Z_POH SAP DATA"
            responses:
              "48377884-24f2-4609-9643-dd0fd419b511":
                status: "200"
                description: "Result OK"
                bodies:
                - type: "#/contract/types/05c5b5be-66b3-40c8-9f4c-75d9327d5566"
                  examples:
                  - value: |-
                      {
                      "SAP_Z_POH":[
                          {
                              "Client": "100",
                              "Purchase Order": "4500004361",
                              "Purchasing Doc. Type": "ZB",
                              "Purchase Order Date": "2025-02-01",
                              "Total val. upon release": "7652452"
                          },
                          {
                              "Client": "100",
                              "Purchase Order": "4500004361",
                              "Purchasing Doc. Type": "ZB",
                              "Purchase Order Date": "2025-02-27",
                              "Total val. upon release": "7652452"
                          }
                      ]
                      }
                  mediaTypes:
                  - "application/json"
      ea87eef0-bdfa-452e-9ae4-58c852158dc5:
        path: "/Z_POH/{Client}"
        pathVariables:
        - name: "Client"
          type: "STRING"
          required: true
        operations:
          "2fd3f3cb-1900-4e98-8254-3b590b4bf785":
            name: "Filter_SAP_Z_POH"
            method: "GET"
            queryParameters:
            - name: "dateFrom"
              type: "DATE"
              required: false
              examples:
              - value: "2025-02-01"
            - name: "dateTo"
              type: "DATE"
              required: false
              examples:
              - value: "2025-02-01"
            responses:
              "5308a918-1624-4f9f-b0c4-2209d0c96617":
                status: "200"
                description: "It ok"
                bodies:
                - type: "#/contract/types/470db667-d635-4208-803d-db908e61d301"
                  examples:
                  - value: |-
                      {
                      "SAP_Z_POH":[
                          {
                              "Client": "100",
                              "Purchase Order": "4500004361",
                              "Purchasing Doc. Type": "ZB",
                              "Purchase Order Date": "2025-02-01",
                              "Total val. upon release": "7652452"
                          },
                          {
                              "Client": "100",
                              "Purchase Order": "4500004361",
                              "Purchasing Doc. Type": "ZB",
                              "Purchase Order Date": "2025-02-27",
                              "Total val. upon release": "7652452"
                          }
                      ]
                      }
                  mediaTypes:
                  - "application/json"
    types:
      "470db667-d635-4208-803d-db908e61d301":
        name: "SAP_Z_POH_FILTRED"
        type: "OBJECT"
        description: "Filtred data from SAP_Z_POH"
        required: false
        properties:
        - name: "SAP_Z_POH"
          type: "ARRAY"
          required: false
          items:
            type: "OBJECT"
            required: false
            properties:
            - name: "Client"
              type: "STRING"
              required: false
            - name: "Purchase Order"
              type: "STRING"
              required: false
            - name: "Purchasing Doc. Type"
              type: "STRING"
              required: false
            - name: "Purchase Order Date"
              type: "DATE"
              required: false
            - name: "Total val. upon release"
              type: "STRING"
              required: false
        examples:
        - value: "{\r\n\"SAP_Z_POH\":[\r\n    {\r\n        \"Client\": \"100\",\r\n        \"Purchase Order\": \"4500004361\",\r\n        \"Purchasing Doc. Type\": \"ZB\",\r\n        \"Purchase Order Date\": \"2025-02-01\",\r\n        \"Total val. upon release\": \"7652452\"\r\n    },\r\n    {\r\n        \"Client\": \"100\",\r\n        \"Purchase Order\": \"4500004361\",\r\n        \"Purchasing Doc. Type\": \"ZB\",\r\n        \"Purchase Order Date\": \"2025-02-27\",\r\n        \"Total val. upon release\": \"7652452\"\r\n    }\r\n]\r\n}"
      "05c5b5be-66b3-40c8-9f4c-75d9327d5566":
        name: "SAP_Z_POH"
        type: "OBJECT"
        description: "SAP_Z_POH DATA"
        required: false
        properties:
        - name: "SAP_Z_POH"
          type: "ARRAY"
          required: false
          items:
            type: "OBJECT"
            required: false
            properties:
            - name: "Client"
              type: "INTEGER"
              required: true
            - name: "Purchase Order"
              type: "STRING"
              required: true
            - name: "Purchasing Doc. Type"
              type: "STRING"
              required: false
            - name: "Purchase Order Date"
              type: "DATE"
              required: false
            - name: "Total val. upon release"
              type: "NUMBER"
              required: false
        examples:
        - value: |-
            {
            "SAP_Z_POH":[
                {
                    "Client": "100",
                    "Purchase Order": "4500004361",
                    "Purchasing Doc. Type": "ZB",
                    "Purchase Order Date": "2025-02-01",
                    "Total val. upon release": "7652452"
                },
                {
                    "Client": "100",
                    "Purchase Order": "4500004361",
                    "Purchasing Doc. Type": "ZB",
                    "Purchase Order Date": "2025-02-27",
                    "Total val. upon release": "7652452"
                }
            ]
            }
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "SAP_EXTRACT_TEST 1.0.0",
        "description" : "No description",
        "importedFrom" : "fd857daa-675c-418f-b8cd-ed6a47e0e59b"
      },
      "children" : [ {
        "entity" : {
          "type" : "Request",
          "id" : "ac8c3ab8-f37f-4089-bed3-b4295a30c7cb",
          "name" : "Add Customer",
          "uri" : {
            "host" : "${\"BaseUrl\"}",
            "path" : "/Customer"
          },
          "method" : {
            "link" : "",
            "name" : "POST",
            "requestBody" : true
          },
          "headers" : [ {
            "enabled" : true,
            "name" : "Content-Type",
            "value" : "application/json"
          } ],
          "headersType" : "Form",
          "body" : {
            "bodyType" : "Text",
            "textBody" : "{\"ID\": \"1920\",\n\"NAME\": \"Sofiene\",\n\"LAST NAME\": \"Khayati\",\n\"MAIL\": \"Sofiene.Khayati@agilos.com\",\n\"PHONE\": \"0465784646\",\n\"STREET_NUMBER\": \"12\",\n\"CITY\": \"Ixelles\",\n\"DEPARTMENT\": \"Brussels\",\n\"REGION\": \"Brussels\",\n\"COUNTRY\": \"Belgium\",\n\"POSTAL_CODE\": \"1050\"}"
          }
        }
      }, {
        "entity" : {
          "type" : "Request",
          "id" : "a6b9e8da-e3be-4472-b4f3-03be430a009b",
          "name" : "SAP_Z_POH",
          "description" : "Z_POH SAP DATA",
          "uri" : {
            "host" : "${\"BaseUrl\"}",
            "path" : "/Z_POH"
          },
          "method" : {
            "link" : "",
            "name" : "GET"
          },
          "headers" : [ {
            "enabled" : true,
            "name" : "Accept",
            "value" : "application/json"
          } ],
          "headersType" : "Form"
        }
      }, {
        "entity" : {
          "type" : "Request",
          "id" : "2fd3f3cb-1900-4e98-8254-3b590b4bf785",
          "name" : "Filter_SAP_Z_POH",
          "uri" : {
            "host" : "${\"BaseUrl\"}",
            "path" : "/Z_POH/{Client}",
            "query" : {
              "delimiter" : "&",
              "items" : [ {
                "name" : "dateFrom",
                "value" : "2025-02-01",
                "enabled" : false
              }, {
                "name" : "dateTo",
                "value" : "2025-02-01",
                "enabled" : false
              } ]
            }
          },
          "method" : {
            "link" : "",
            "name" : "GET"
          },
          "headers" : [ {
            "enabled" : true,
            "name" : "Accept",
            "value" : "application/json"
          } ],
          "headersType" : "Form",
          "uriEditor" : true
        }
      } ]
    } ],
    "environments" : [ {
      "name" : "SAP_EXTRACT_TEST 1.0.0",
      "importedFrom" : {
        "projectId" : "fd857daa-675c-418f-b8cd-ed6a47e0e59b"
      },
      "variables" : {
        "f84f5e35-4abf-43aa-b51e-ca6fa0a0c93f" : {
          "name" : "BaseUrl",
          "value" : "https://2ig912ru1eka29u.eu.api-mocks.com",
          "enabled" : true,
          "private" : false
        }
      }
    }, {
      "name" : "SAP_EXTRACT_TEST 1.0.0",
      "importedFrom" : {
        "projectId" : "fd857daa-675c-418f-b8cd-ed6a47e0e59b"
      },
      "variables" : {
        "ab3ad42e-222e-417a-a7af-d109c5d30e91" : {
          "name" : "BaseUrl",
          "value" : "http://www.agilos.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
