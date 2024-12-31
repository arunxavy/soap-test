# SOAP API to Retrieve List of Countries

This project provides a simple SOAP-based web service to retrieve a static list of countries using Java and Spring Boot. The implementation follows best coding practices to ensure maintainability and clarity.

## Features

- SOAP web service implemented with Spring Boot.
- JAXB for XML serialization and deserialization.
- WSDL generation for service contract.
- Easy configuration and deployment.

## Getting Started

### Prerequisites

- Java 17 or later
- Maven 3.6 or later

### Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/your-repository/countries-api.git
   cd countries-api
   ```

2. Build the project:

   ```bash
   mvn clean install
   ```

3. Run the application:

   ```bash
   mvn spring-boot:run
   ```

4. Access the WSDL at:

   ```
   http://localhost:8080/ws/countries.wsdl
   ```

## API Details

### Namespace

- `http://example.com/countriesapi`

### Operations

#### GetCountries

**Request**: `GetCountriesRequest`

**Response**: `GetCountriesResponse`

The response contains a list of static country names.

### Example Request (SOAP XML)

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ns="http://example.com/countriesapi">
   <soapenv:Header/>
   <soapenv:Body>
      <ns:GetCountriesRequest/>
   </soapenv:Body>
</soapenv:Envelope>
```

### Example Response (SOAP XML)

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ns="http://example.com/countriesapi">
   <soapenv:Header/>
   <soapenv:Body>
      <ns:GetCountriesResponse>
         <countries>United States</countries>
         <countries>Canada</countries>
         <countries>Mexico</countries>
         <countries>United Kingdom</countries>
         <countries>Germany</countries>
         <countries>France</countries>
         <countries>India</countries>
         <countries>China</countries>
         <countries>Japan</countries>
         <countries>Australia</countries>
      </ns:GetCountriesResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Project Structure

- **CountriesApiApplication**: Main Spring Boot application class.
- **WebServiceConfig**: Configuration for SOAP WSDL and schema.
- **CountriesEndpoint**: SOAP endpoint to handle requests.
- **GetCountriesRequest**: Request object for the API.
- **GetCountriesResponse**: Response object for the API.

## Extending the Service

1. Add new endpoints by creating new methods in the `CountriesEndpoint` class.
2. Update the WSDL configuration as needed.
3. Regenerate WSDL by restarting the application.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For any issues or enhancements, please raise an issue in the repository.

