# NestJS Prisma Module

# Usage

app.module.ts:
```ts
import { PrismaModule } from '@onlynices/nest-prisma';

@Module({
  imports: [PrismaModule],
  providers: [AppService]
})
export class AppModule {}
```

app.service.ts:
```ts
import { PrismaService } from '@onlynices/nest-prisma';

@Injectable()
export class AppService {
  constructor(private readonly prisma: PrismaService) {}

  async fetchSomething() {
    return this.prisma.something.findMany();
  }

  // ...
}
```