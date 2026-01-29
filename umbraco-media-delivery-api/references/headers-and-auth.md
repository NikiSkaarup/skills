# Headers and Auth

## Api-Key

- Required when public access is disabled.
- Media API access cannot be more permissive than Delivery API access.

## Access Configuration Notes

- Media Delivery API requires `DeliveryApi:Enabled` to be true.
- `DeliveryApi:Media` can only be more restrictive than `DeliveryApi`.
