# Todo Tutorial

[Claude Code Playbook](https://docs.claude-hunt.com) 강의에서 작은 할 일 앱을 직접 만들어 보며 Claude Code 쓰는 법을 배우는 연습용 저장소입니다.

## 관련 링크

- 강의 본문: https://docs.claude-hunt.com
- 수강생 결과물 공유: https://claude-hunt.com

## 기술 스택

- Next.js 16 (App Router, Turbopack)
- React 19
- Tailwind CSS v4
- shadcn/ui (radix-maia 스타일, taupe 베이스)
- TypeScript / ESLint / Prettier
- 패키지 매니저: bun 1.3.6

## 시작하기

### 사전 준비

- [Git](https://git-scm.com)
- [bun](https://bun.sh) (이 저장소는 bun 1.3.6 기준이며, 설치 후 `bun --version`으로 확인하세요.)
- Node.js (Next.js가 사용합니다. 현재 LTS 이상을 권장합니다.)

### 설치와 실행

```bash
git clone <저장소 주소>
cd <저장소 폴더>
bun install
bun run dev
```

개발 서버가 뜨면 브라우저에서 [http://localhost:3000](http://localhost:3000) 을 여세요. 종료는 터미널에서 `Ctrl + C`입니다.

3000번 포트를 이미 쓰고 있다면 Next.js가 다른 포트(예: 3001)로 띄우고 터미널에 주소를 알려 줍니다.

### 설치가 잘 됐는지 확인

```bash
bun run test       # 테스트
bun run typecheck  # 타입 검사
bun run lint       # ESLint
```

세 명령이 모두 오류 없이 끝나면 준비가 끝난 것입니다.

### 자주 쓰는 스크립트

```bash
bun run dev        # 개발 서버
bun run build      # 프로덕션 빌드
bun run start      # 빌드 결과 실행 (먼저 build 필요)
bun run test       # 테스트 한 번 실행
bun run test:watch # 테스트 감시 모드
bun run lint       # ESLint
bun run typecheck  # tsc --noEmit
bun run format     # Prettier 포맷팅
```

## 레슨별 시작 브랜치

레슨마다 시작 시점의 코드를 `lesson/<레슨 이름>` 브랜치로 제공합니다. 레슨 본문이 안내하는 브랜치로 바꾼 뒤 따라가세요.

```shell
git checkout lesson/claude-md
```

## 컴포넌트 추가

shadcn/ui 컴포넌트는 다음과 같이 추가합니다.

```bash
bunx --bun shadcn@latest add button
```

`components/ui` 디렉토리에 컴포넌트가 추가됩니다.

## 컴포넌트 사용

```tsx
import { Button } from "@/components/ui/button";
```
