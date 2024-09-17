>demo.service.ts

```TS
import { Injectable } from '@nestjs/common';

@Injectable()
export class DemoService {
	constructor() {}

	async returnDemo(): Promise<any> {
	  return 'demo';
	}
}
```

>demo.service.spec.ts

```TS
import { Test, TestingModule } from '@nestjs/testing';
import { DemoService } from './demo.service';
import { RootTestModule } from '@noloback/root.test';

describe('DemoService', () => {
  let service: DemoService;

  beforeEach(async () => {
    const module: TestingModule = await Test.createTestingModule({
      providers: [DemoService],
      imports: [RootTestModule],
    }).compile();

    service = module.get<DemoService>(DemoService);
  });

  it('should be defined', () => {
    expect(service).toBeDefined();
  });
});
```
