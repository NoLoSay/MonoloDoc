>demo.controller.ts
```TS
import { Controller } from '@nestjs/common';

@Controller('demo')
export class DemoService {
	constructor(private readonly demoService: DemoService) {}

	@Get()
	async getDemo() {
	  return demoService.returnDemo();
	}
}
```

>demo.controller.spec.ts
```TS
import { Test, TestingModule } from '@nestjs/testing';
import { DemoController } from './demo.controller';
import { DemoService } from '@noloback/demo.service';
import { RootTestModule } from '@noloback/root.test';

describe('DemoController', () => {
  let controller: DemoController;

  beforeEach(async () => {
    const module: TestingModule = await Test.createTestingModule({
      controllers: [DemoController],
      providers: [DemoService],
      imports: [RootTestModule],
    }).compile();

    controller = module.get<DemoController>(DemoController);
  });

  it('should be defined', () => {
    expect(controller).toBeDefined();
  });
});
```
