# README

COMANDOS:
  Para instalar as gems presentes neste projeto, digite no terminal o seguinte comando: bundle install

  Para rodar todos os testes presentes na pasta "spec", digite no terminal o seguinte comando: rspec spec/

  Para subir o servidor, digite no terminal o seguinte comando: rails s

  Para executar as migrations, digite no terminal o seguinte comando: rails db:migrate

ENDPOINTS:
  ### Criar um cliente

    endpoint: "/customers"
    verbo HTTP: POST

    request body:
    {
      "name": "Jane Doe"
    }

    response body:
    {
      "id": 6,
      "name": "Jane Doe"
    }

    status code: 201 (created)

=================================================================

  ### Criar um empréstimo

    endpoint: "/loans"
    verbo HTTP: POST

    request body:
      {
        "total_value",
        "total_installment",
        "customer_id"
      }

    response body:

      {
        "id": 2,
        "total_value": "3000.0",
        "total_installment": 2,
        "customer_name": "John Doe",
        "installments": [
          {
            "id": 5,
            "parcel_price": "1500.0",
            "parcel_number": 1
          },
          {
            "id": 6,
            "parcel_price": "1500.0",
            "parcel_number": 2
          }
        ]
      }

      status code: 201 (created)

=================================================================

  ### Mostrar um empréstimo

    endpoint: "/loans/:id"
    verbo HTTP: GET

    response body:

      {
        "id": 2,
        "total_value": "3000.0",
        "total_installment": 2,
        "customer_name": "John Doe",
        "installments": [
          {
            "id": 5,
            "parcel_price": "1500.0",
            "parcel_number": 1
          },
          {
            "id": 6,
            "parcel_price": "1500.0",
            "parcel_number": 2
          }
        ]
      }

      status code: 200 (ok)
