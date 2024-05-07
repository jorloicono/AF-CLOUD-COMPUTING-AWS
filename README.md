https://435562384942.signin.aws.amazon.com/console?region=us-east-1

Whiz_User_104685.41685904

a8e64dac-513a-4d46-a54d-d441fb2aa379

AWSTemplateFormatVersion: '2010-09-09'
Parameters:
  VpcCIDR:
    Description: CIDR block fortheVPC
    Type: String
    Default: "10.0.0.0/16" # Puedes cambiar este valor por defecto si quieres
    AllowedPattern: "(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})\\.(\\d{1,3})/(\\d{1,2})"
    ConstraintDescription: Debe ser un rango CIDR válido (por ejemplo, 10.0.0.0/16)
Resources:
  MyVPC:
    Type: AWS::EC2::VPC
    Properties:
      CidrBlock: !Ref VpcCIDR
      EnableDnsSupport: true
      EnableDnsHostnames: true
      Tags:
        - Key: Name
          Value: MyVPC

# Módulo 1: Introducción a AWS y Comparación con Azure

- Visión general detallada de la infraestructura de AWS.
- Comparación de servicios de cómputo, almacenamiento y redes en AWS y Azure.
- Estrategias de migración: Identificación de casos de uso específicos.

# Módulo 2: Fundamentos de AWS y Servicios Básicos

- EC2: Servicios de cómputo e implementación de instancias de VM
- S3: Servicio de almacenamiento y comparación con Azure Blob Storage.
- RDS: Configuración y administración de bases de datos.
- IAM: Gestión de identidades, roles y políticas
- Networking en AWS: Profundización en VPCs, subnets, Route 53

# Módulo 3: Servicios Avanzados de AWS

- AWS Lambda y Serverless: Desarrollo y despliegue de funciones sin servidor, comparación con Azure Functions.
- Amazon DynamoDB: NoSQL en AWS y comparación con Azure Cosmos DB.
- AWS Elastic Beanstalk: Despliegue y administración de aplicaciones.

# Módulo 4: Big Data y Machine Learning en AWS

- Amazon EMR: Configuración y procesamiento de big data.
- Amazon SageMaker: Desarrollo de modelos de machine learning, entrenamiento e implementación.
- Comparación detallada de servicios de big data y machine learning en AWS y Azure
