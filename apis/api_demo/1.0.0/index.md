---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "API_DEMO"
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
    - "#/contract/resources/bd6f7e83-ab55-46a1-89f7-169bb3d38c0c"
    - "#/contract/resources/c71d6a04-ed87-40a1-a33b-21e12e24d4e2"
    - "#/contract/resources/d082c386-2a67-47cd-a0ad-2f900637dbe2"
    - "#/contract/types/448efcb2-760a-41c0-93eb-2e42edca3cca"
    - "#/contract/types/a824867f-c7a3-4a7d-bb63-a114f0ce75b4"
    resources:
      bd6f7e83-ab55-46a1-89f7-169bb3d38c0c:
        path: "/Customers"
        operations:
          "57bbc097-942c-4dbb-8b35-607f10493b89":
            name: "List Customers"
            method: "GET"
            description: "List All customers"
            responses:
              ce69790f-a97b-4620-b19d-26fa2a78904b:
                status: "200"
                description: "Result OK"
                bodies:
                - type: "#/contract/types/a824867f-c7a3-4a7d-bb63-a114f0ce75b4"
                  examples:
                  - value: |-
                      {
                      "Customers":[
                          {
                              "ID": "1234",
                              "NAME": "Alice",
                              "LAST_NAME": "Khayati",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "11",
                              "CITY": "Brussels",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1000"
                          },
                          {
                              "ID": "1920",
                              "NAME": "Sofiene",
                              "LAST_NAME": "Khayati",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "12",
                              "CITY": "Ixelles",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1050"
                          },
                          {
                              "ID": "1920",
                              "NAME": "Lina",
                              "LAST_NAME": "Khayati",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "12",
                              "CITY": "Ixelles",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1050"
                          },
                          {
                              "ID": "1920",
                              "NAME": "Henri",
                              "LAST_NAME": "Van Den Berghe",
                              "MAIL": "Sofiene.Khayati@agilos.com",
                              "PHONE": "0465784646",
                              "STREET_NUMBER": "1",
                              "CITY": "Saint Gilles",
                              "DEPARTMENT": "Brussels",
                              "REGION": "Brussels",
                              "COUNTRY": "Belgium",
                              "POSTAL_CODE": "1060"
                          }
                      ]
                      }
                  mediaTypes:
                  - "application/json"
      c71d6a04-ed87-40a1-a33b-21e12e24d4e2:
        path: "/Customer"
        operations:
          "24a7a629-f739-41f7-9102-2468daf7cdb5":
            name: "Add Customer"
            method: "POST"
            bodies:
            - type: "#/contract/types/448efcb2-760a-41c0-93eb-2e42edca3cca"
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
              a89161a1-4e00-4ddc-9693-c96509559236:
                status: "200"
                description: "Customer Added"
      d082c386-2a67-47cd-a0ad-2f900637dbe2:
        path: "/Customer/{ID}"
        pathVariables:
        - name: "ID"
          type: "STRING"
          required: true
        operations:
          fec49c85-fa60-4e26-bb40-9d53490ef491:
            name: "Get One Custome"
            method: "GET"
            responses:
              b459dc15-774d-4839-bb66-1b6cf4b7b892:
                status: "200"
                description: "It ok"
                bodies:
                - type: "#/contract/types/448efcb2-760a-41c0-93eb-2e42edca3cca"
                  examples:
                  - value: |-
                      {"ID": "1234",
                      "NAME": "Alice",
                      "LAST NAME": "Khayati",
                      "MAIL": "Sofiene.Khayati@agilos.com",
                      "PHONE": "0465784646",
                      "STREET_NUMBER": "11",
                      "CITY": "Brussels",
                      "DEPARTMENT": "Brussels",
                      "REGION": "Brussels",
                      "COUNTRY": "Belgium",
                      "POSTAL_CODE": "1000"}
                  mediaTypes:
                  - "application/json"
    types:
      "448efcb2-760a-41c0-93eb-2e42edca3cca":
        name: "Customer"
        type: "OBJECT"
        description: "Customer informations"
        properties:
        - name: "ID"
          type: "INTEGER"
          format: "INT32"
          description: "Customer ID"
          required: true
        - name: "NAME"
          type: "STRING"
          description: "Customer Name"
          required: true
        - name: "LAST NAME"
          type: "STRING"
          description: "Customer Last Name"
          required: true
        - name: "MAIL"
          type: "STRING"
          description: "Customer Email"
        - name: "PHONE"
          type: "STRING"
          description: "Customer Phone"
        - name: "STREET_NUMBER"
          type: "STRING"
          description: "Customer Adress Street Number"
        - name: "CITY"
          type: "STRING"
          description: "Customer City"
        - name: "DEPARTMENT"
          type: "STRING"
          description: "Customer Department"
        - name: "REGION"
          type: "STRING"
          description: "Customer Region"
        - name: "COUNTRY"
          type: "STRING"
          description: "Customer Country"
        - name: "POSTAL_CODE"
          type: "INTEGER"
          format: "INT32"
          description: "Customer Zip Code"
        examples:
        - value: "{\r\n\"ID\": \"000001\",\r\n\"NAME\": \"Sofiene\",\r\n\"LAST NAME\": \"Khayati\",\r\n\"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n\"PHONE\": \"0465784646\",\r\n\"STREET_NUMBER\": \"1\",\r\n\"CITY\": \"Ixelles\",\r\n\"DEPARTMENT\": \"Brussels\",\r\n\"REGION\": \"Brussels\",\r\n\"COUNTRY\": \"Belgium\",\r\n\"POSTAL_CODE\": \"1050\"\r\n}"
      a824867f-c7a3-4a7d-bb63-a114f0ce75b4:
        name: "Customers"
        type: "OBJECT"
        description: "List Customers"
        properties:
        - name: "Customers"
          type: "ARRAY"
          items:
            type: "OBJECT"
            properties:
            - name: "ID"
              type: "STRING"
            - name: "NAME"
              type: "STRING"
            - name: "LAST_NAME"
              type: "STRING"
            - name: "MAIL"
              type: "STRING"
            - name: "PHONE"
              type: "STRING"
            - name: "STREET_NUMBER"
              type: "STRING"
            - name: "CITY"
              type: "STRING"
            - name: "DEPARTMENT"
              type: "STRING"
            - name: "REGION"
              type: "STRING"
            - name: "COUNTRY"
              type: "STRING"
            - name: "POSTAL_CODE"
              type: "STRING"
        examples:
        - value: "{\r\n\"Customers\":[\r\n    {\r\n        \"ID\": \"1234\",\r\n        \"NAME\": \"Alice\",\r\n        \"LAST_NAME\": \"Khayati\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"11\",\r\n        \"CITY\": \"Brussels\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1000\"\r\n    },\r\n    {\r\n        \"ID\": \"1920\",\r\n        \"NAME\": \"Sofiene\",\r\n        \"LAST_NAME\": \"Khayati\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"12\",\r\n        \"CITY\": \"Ixelles\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1050\"\r\n    },\r\n    {\r\n        \"ID\": \"1920\",\r\n        \"NAME\": \"Lina\",\r\n        \"LAST_NAME\": \"Khayati\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"12\",\r\n        \"CITY\": \"Ixelles\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1050\"\r\n    },\r\n    {\r\n        \"ID\": \"1920\",\r\n        \"NAME\": \"Henri\",\r\n        \"LAST_NAME\": \"Van Den Berghe\",\r\n        \"MAIL\": \"Sofiene.Khayati@agilos.com\",\r\n        \"PHONE\": \"0465784646\",\r\n        \"STREET_NUMBER\": \"1\",\r\n        \"CITY\": \"Saint Gilles\",\r\n        \"DEPARTMENT\": \"Brussels\",\r\n        \"REGION\": \"Brussels\",\r\n        \"COUNTRY\": \"Belgium\",\r\n        \"POSTAL_CODE\": \"1060\"\r\n    }\r\n]\r\n}"
  components: {}
api-tryin: |-
  {
    "version" : 6,
    "entities" : [ {
      "entity" : {
        "type" : "Project",
        "name" : "API_DEMO 1.0.0",
        "description" : "No description",
        "importedFrom" : "734b112a-2a3a-46fc-89ba-8020878eed42"
      },
      "children" : [ {
        "entity" : {
          "type" : "Request",
          "id" : "57bbc097-942c-4dbb-8b35-607f10493b89",
          "name" : "List Customers",
          "description" : "List All customers",
          "uri" : {
            "host" : "${\"BaseUrl\"}",
            "path" : "/Customers"
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
          "id" : "24a7a629-f739-41f7-9102-2468daf7cdb5",
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
          "id" : "fec49c85-fa60-4e26-bb40-9d53490ef491",
          "name" : "Get One Custome",
          "uri" : {
            "host" : "${\"BaseUrl\"}",
            "path" : "/Customer/{ID}"
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
      } ]
    } ],
    "environments" : [ {
      "name" : "API_DEMO 1.0.0",
      "importedFrom" : {
        "projectId" : "734b112a-2a3a-46fc-89ba-8020878eed42"
      },
      "variables" : {
        "23079b7a-429d-40f9-a3d0-a6fe055b1379" : {
          "name" : "BaseUrl",
          "value" : "https://2ig912ru1eka29u.eu.api-mocks.com",
          "enabled" : true,
          "private" : false
        }
      }
    }, {
      "name" : "API_DEMO 1.0.0",
      "importedFrom" : {
        "projectId" : "734b112a-2a3a-46fc-89ba-8020878eed42"
      },
      "variables" : {
        "116face0-db8f-4061-92d5-fb5dd06ef018" : {
          "name" : "BaseUrl",
          "value" : "http://www.agilos.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
