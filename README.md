# WaaC Configuration Guide

This guide explains how to use and customize the WaaC (Warehouse as a Code) configuration file for managing warehouse operations.

## Overview

The WaaC configuration file is a YAML-based definition that allows you to describe and manage:
- Physical warehouse layout
- Logical storage configurations
- Multi-tenant operations
- Warehouse processes (inbound, outbound, picking, packing, loading)
- Cross-docking operations
- Master data management

## File Structure

The configuration is organized into several main sections:

```yaml
version: '1.1'
physical_layout:     # Physical warehouse configuration
tag_catalog:        # Available tags for classification
tenants:           # Tenant-specific configurations
filter_rules:      # Rules for filtering storage locations
validation_rules:  # System-wide validation rules
```

## Physical Layout Configuration

The `physical_layout` section defines the physical structure of your warehouse:

```yaml
physical_layout:
  warehouse_id: 'WH001'
  buildings:
    building_1:
      areas:
        area_A:
          racks:
            rack_A1:
              type: 'selective_pallet_rack'
              physical_properties:
                length: 30000  # mm
                height: 8000   # mm
                depth: 1100    # mm
```

### Key Components:
- Buildings
- Areas
- Racks
- Physical dimensions
- Storage capacities
- Equipment requirements

## Tag System

The `tag_catalog` defines available tags for classifying warehouse locations:

```yaml
tag_catalog:
  location:
    values: ['front_area', 'back_area', 'mezzanine', 'ground_floor']
    type: 'single'
  
  access:
    values: ['easy_reach', 'specialized', 'restricted']
    type: 'single'
```

Tags help in:
- Organizing storage locations
- Defining access requirements
- Specifying equipment needs
- Managing environmental conditions

## Tenant Configuration

Each tenant can have specific configurations:

```yaml
tenants:
  - id: 'fast_fashion'
    name: 'FastFashion SpA'
    type: 'e-commerce'
    logical_layout:
      zones:
        fast_moving:
          description: 'Zona alta rotazione'
          storage_filters:
            location:
              include: ['front_area']
```

### Tenant Features:
- Logical layout definition
- Storage filters
- Connection configurations
- Operation specifications

## Warehouse Operations

### 1. Inbound Operations
```yaml
inbound:
  receiving:
    modes:
      - type: 'asn'
        enabled: true
      - type: 'no_asn'
        enabled: true
```

### 2. Outbound Operations
```yaml
outbound:
  picking_wave:
    types:
      - type: 'automatic'
      - type: 'manual'
```

### 3. Picking Operations
```yaml
picking:
  types:
    fixed:
      enabled: true
    dynamic:
      enabled: true
    bulk:
      enabled: true
```

### 4. Packing Operations
```yaml
packing:
  order_consolidation:
    enabled: true
  packaging:
    enabled: true
```

## Customization

1. **Physical Layout**: Adjust dimensions, capacities, and structure based on your warehouse
2. **Tags**: Modify the tag catalog to match your classification needs
3. **Tenants**: Configure tenant-specific rules and operations
4. **Operations**: Enable/disable features and adjust parameters

## Validation Rules

The system includes built-in validation rules:

```yaml
validation_rules:
  physical:
    - rule: 'structural_integrity'
  logical:
    - rule: 'zone_assignment'
```

These ensure:
- Physical constraints are respected
- Logical assignments are valid
- Safety requirements are met
- Operational efficiency is maintained

## Best Practices

1. **Physical Layout**
   - Define accurate measurements
   - Include all safety requirements
   - Specify equipment needs

2. **Tenant Configuration**
   - Use clear zone descriptions
   - Define precise storage filters
   - Set appropriate constraints

3. **Operations**
   - Enable only needed features
   - Configure appropriate limits
   - Set realistic constraints

4. **Tags**
   - Use meaningful classifications
   - Maintain consistent naming
   - Define clear hierarchies

## Environment Variables

The configuration supports environment variables for sensitive data:
```yaml
credentials:
  username: '${ENV_FTP_USER}'
  password: '${ENV_FTP_PASS}'
```

Replace these placeholders with actual values in your environment.

## Validation

Before deploying, ensure:
1. All required fields are completed
2. Physical constraints are realistic
3. Tenant configurations don't conflict
4. Operations are properly configured
5. Environment variables are set

This configuration file provides a complete definition of your warehouse operations, enabling automated management and optimization of warehouse processes.
