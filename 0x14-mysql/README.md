# MySQL Primary-Replica Setup

This project implements a Primary-Replica infrastructure using MySQL. The setup includes configuration of two servers: a primary database server and a replica server, along with backup functionality.

## Server Information
- Primary (web-01): `34.207.212.172`
- Replica (web-02): `18.210.13.214`
- Load Balancer: `52.72.19.22`

## Project Structure
- `4-mysql_configuration_primary`: MySQL configuration for primary server
- `4-mysql_configuration_replica`: MySQL configuration for replica server
- `5-mysql_backup`: Backup script for MySQL database

## Features
- MySQL 5.7 installation
- Database replication
- Automated backup system
- User management with specific privileges
- Custom database and table creation

## Requirements
- Ubuntu 16.04 LTS
- MySQL 5.7.x
- UFW (Uncomplicated Firewall)
