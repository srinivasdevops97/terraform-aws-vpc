# Terraform AWS VPC Module Customised

This module is going to create the following resources. For high availability, we are going to get first 2 availability zones.

* VPC
* Internet Gateway associated with VPC
* 2 Public subnets
* 2 Private subnets
* 2 database subnets
* Database subnet group
* EIP
* NAT gateway
* Public Route table
* Private Route table
* Database Route table
* Routes
* Route tables associations with subnets
* Peering with default VPC(if Required)
* Peering routes in acceptor and requestor route tables

# Inputs
* project_name (Mandatory): User must supply their project_name
* environment (Mandatory): User must supply their project_name
* vpc_cidr (Mandatory): User must supply their project_name
* enable_dns_hostnames (Optional): Default to true
* common_tags (Optional): Default is empty. user can supply tags in list(string) format
* vpc_tags (Optional): Default is empty. user can supply tags in list(string) format
* igw_tags (Optional): Default is empty. user can supply tags in list(string) format
* public_subnet_cidrs (Mandatory): User must supply only 2 valid public subnet CIDR
* public_subnet_tags (Optional): Default is empty. user can supply tags in list(string) format
* private_subnet_cidrs (Mandatory): User must supply only 2 valid private subnet CIDR
* private_subnet_tags (Optional): Default is empty. user can supply tags in list(string) format
* database_subnet_cidrs (Mandatory): User must supply only 2 valid database subnet CIDR
* database_subnet_tags (Optional): Default is empty. user can supply tags in list(string) format
* db_subnet_group_tags (Optional): Default is empty. user can supply tags in list(string) format
* nat_gateway_tags (Optional): Default is empty. user can supply tags in list(string) format
* public_route_table_tags (Optional): Default is empty. user can supply tags in list(string) format
* private_route_table_tags (Optional): Default is empty. user can supply tags in list(string) format
* database_route_table_tags (Optional): Default is empty. user can supply tags in list(string) format
* is_peering_required (Optional): Defaults to false
* vpc_peering_tags (Optional): Default is empty. user can supply tags in list(string) format

# outputs
* vpc_id : VPC ID created
* public_subnet_ids : list of 2 public subnet ids created
* private_subnet_ids : list of 2 private subnet ids created
* database_subnet_ids : list of 2 database subnet ids created