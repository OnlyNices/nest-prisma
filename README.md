# NestJS Prisma Module

# Usage
Example

app.module.ts:

import { PrismaModule } from '@onlynices/nest-prisma';

@Module({
  imports: [PrismaModule],
  providers: [AppService]
})
export class AppModule {}

app.service.ts:

import { PrismaService } from '@onlynices/nest-prisma';

@Injectable()
export class AppService {
  constructor(private readonly prisma: PrismaService) {}

  // ...
}