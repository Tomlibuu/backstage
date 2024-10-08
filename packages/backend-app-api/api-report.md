## API Report File for "@backstage/backend-app-api"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts
import { BackendFeature } from '@backstage/backend-plugin-api';
import { IdentityService } from '@backstage/backend-plugin-api';
import { ServiceFactory } from '@backstage/backend-plugin-api';
import { ServiceFactoryCompat } from '@backstage/backend-plugin-api';
import { TokenManagerService } from '@backstage/backend-plugin-api';

// @public (undocumented)
export interface Backend {
  // (undocumented)
  add(
    feature:
      | BackendFeature
      | Promise<{
          default: BackendFeature;
        }>,
  ): void;
  // (undocumented)
  start(): Promise<void>;
  // (undocumented)
  stop(): Promise<void>;
}

// @public (undocumented)
export function createSpecializedBackend(
  options: CreateSpecializedBackendOptions,
): Backend;

// @public (undocumented)
export interface CreateSpecializedBackendOptions {
  // (undocumented)
  defaultServiceFactories: ServiceFactory[];
}

// @public @deprecated
export type IdentityFactoryOptions = {
  issuer?: string;
  algorithms?: string[];
};

// @public @deprecated (undocumented)
export const identityServiceFactory: ServiceFactoryCompat<
  IdentityService,
  'plugin',
  'singleton',
  IdentityFactoryOptions
>;

// @public @deprecated (undocumented)
export const tokenManagerServiceFactory: ServiceFactoryCompat<
  TokenManagerService,
  'plugin',
  'singleton',
  undefined
>;
```
