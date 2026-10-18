# AWS VPC Peering Project

## Objective
Connect two Amazon VPCs using VPC Peering and validate private connectivity to an EC2 instance.

## Region
Europe (Stockholm), `eu-north-1`

## Network
- VPC-A: `10.0.0.0/16`
- VPC-B: `10.1.0.0/16`
- Peering connection: `pcx-008dccff0cf5e2620` (Active in supplied evidence)
- Bastion-VPC-A private IP: `10.0.1.124`
- Private-Server-A private IP: `10.0.2.218`
- Private-Server-B private IP: `10.1.1.81`

## Validation
- VPC-A route tables have a route to `10.1.0.0/16` via the peering connection.
- VPC-B private route table has a return route to `10.0.0.0/16` via the peering connection.
- Ping to `10.1.1.81`: 4/4 packets received, 0% packet loss.
- SSH through the bastion succeeded and returned `ip-10-1-1-81`.

## Project contents
- `VPC_Peering_Project_Report.pdf` — report with evidence screenshots
- `VPC_Peering_Configuration.txt` — resource/configuration summary
- `VPC_Peering_Test_Results.txt` — test results
- `VPC-Peering-Evidence/` — seven supplied screenshots

