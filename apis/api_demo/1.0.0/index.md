---
# NOTICE: Copyright 2025 Talend SA, Talend, Inc., and affiliates. All Rights Reserved. Customer’s use of the software contained herein is subject to the terms and conditions of the Agreement between Customer and Talend.
layout: "apiDefinition_1.1.0"
api-definition:
  specVersion: "4.1.0"
  info:
    name: "API_DEMO"
    version: "1.0.0"
    description: "No description"
  contract:
    mediaTypes:
    - "application/json"
    unsortedElementOrder:
    - "#/contract/types/2852090e-4a5e-40d2-8399-7b98060a7a26"
    - "#/contract/types/a1cb4706-ff3f-4c88-ad1f-315c87497703"
    - "#/contract/resources/1e80ed9f-04c0-4c5d-b66a-7d7497298188"
    - "#/contract/resources/3f3f3b75-2842-4381-be18-b192b789a008"
    resources:
      "1e80ed9f-04c0-4c5d-b66a-7d7497298188":
        path: "/Customers"
        operations:
          "7a49026f-0b2a-4d0e-ba42-ea41d3578781":
            name: "List of customer"
            method: "GET"
            responses:
              f8e79199-cddc-4774-9bc2-b296393fb9a3:
                status: "200"
                description: "List found"
                bodies:
                - type: "ARRAY"
                  items:
                    type: "STRING"
                    required: false
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
                          }
                      ]
                      }
                  mediaTypes:
                  - "application/json"
              "214797cc-423d-4b2d-8bb8-c6f2330efdb7":
                status: "404"
                description: "Not Found"
                bodies:
                - type: "OBJECT"
                  description: "Return all customer"
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
      "3f3f3b75-2842-4381-be18-b192b789a008":
        path: "/Customers/{ID}"
        pathVariables:
        - name: "ID"
          type: "STRING"
          required: true
        operations:
          a33cbd28-b630-4155-ba74-1c47648eb8c9:
            name: "Get one customer"
            method: "GET"
            responses:
              "9b2a7850-fca2-48e6-a6dc-206809e1cb6b":
                status: "200"
                description: "Customer retreived"
                bodies:
                - type: "OBJECT"
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
              "27096b0c-3aff-4c53-99f6-7da755bd4174":
                status: "404"
                description: "Customer not found"
    types:
      "2852090e-4a5e-40d2-8399-7b98060a7a26":
        name: "Customer"
        type: "OBJECT"
        properties:
        - name: "ID"
          type: "INTEGER"
          required: true
        - name: "NAME"
          type: "STRING"
          required: true
        - name: "LAST NAME"
          type: "STRING"
          required: true
        - name: "MAIL"
          type: "STRING"
          required: false
        - name: "PHONE"
          type: "STRING"
          required: false
        - name: "STREET"
          type: "STRING"
          required: false
        - name: "CITY"
          type: "STRING"
          required: false
        - name: "DEPARTMENT"
          type: "STRING"
          required: false
        - name: "REGION"
          type: "STRING"
          required: false
        - name: "COUNTRY"
          type: "STRING"
          required: false
        - name: "POSTAL_CODE"
          type: "INTEGER"
          required: false
        examples:
        - value: |-
            {
            "ID": "000001",
            "NAME": "Sofiene",
            "LAST NAME": "Khayati",
            "MAIL": "Sofiene.Khayati@agilos.com",
            "PHONE": "0465784646",
            "STREET_NUMBER": "1",
            "CITY": "Ixelles",
            "DEPARTMENT": "Brussels",
            "REGION": "Brussels",
            "COUNTRY": "Belgium",
            "POSTAL_CODE": "1050"
            }
      a1cb4706-ff3f-4c88-ad1f-315c87497703:
        name: "Customers"
        type: "OBJECT"
        required: false
        properties:
        - name: "Customers"
          type: "ARRAY"
          required: false
          items:
            type: "OBJECT"
            required: false
            properties:
            - name: "ID"
              type: "INTEGER"
              required: true
            - name: "NAME"
              type: "STRING"
              required: true
            - name: "LAST_NAME"
              type: "STRING"
              required: true
            - name: "MAIL"
              type: "STRING"
              required: false
            - name: "PHONE"
              type: "STRING"
              required: false
            - name: "STREET_NUMBER"
              type: "STRING"
              required: false
            - name: "CITY"
              type: "STRING"
              required: false
            - name: "DEPARTMENT"
              type: "STRING"
              required: false
            - name: "REGION"
              type: "STRING"
              required: false
            - name: "COUNTRY"
              type: "STRING"
              required: false
            - name: "POSTAL_CODE"
              type: "INTEGER"
              required: false
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
          "id" : "7a49026f-0b2a-4d0e-ba42-ea41d3578781",
          "name" : "List of customer",
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
          "id" : "a33cbd28-b630-4155-ba74-1c47648eb8c9",
          "name" : "Get one customer",
          "uri" : {
            "host" : "${\"BaseUrl\"}",
            "path" : "/Customers/{ID}"
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
        "07138071-0083-4856-8c16-8a164ae95c1f" : {
          "name" : "BaseUrl",
          "value" : "https://example.com",
          "enabled" : true,
          "private" : false
        }
      }
    } ]
  }
---
