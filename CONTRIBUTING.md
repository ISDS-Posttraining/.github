# Contributing

코드 구조와 프레임워크는 자유입니다. 아래 규칙만 지켜주세요.

## 규칙

1. 레포 이름은 `<method>-repro` 형식의 소문자로 짓습니다. 예: `dpo-repro`, `grpo-repro`
2. README에 아래 결과표를 반드시 넣습니다. 원 레포를 fork한 경우에는 `REPRO.md`를 따로 만들어 넣습니다.
3. 체크포인트, 데이터셋, wandb 로그, `.env`(API 토큰)는 커밋하지 않습니다. 모델 가중치는 Hugging Face에 올리고 링크만 남깁니다.
4. 원 저자 코드를 가져다 쓴 경우 출처와 원 라이선스를 README에 표기합니다.
5. 레포는 private으로 시작하고, 결과가 정리되면 public으로 전환합니다.
6. 레포를 만들면 [org 프로필 README](https://github.com/ISDS-Posttraining/.github/blob/main/profile/README.md)의 표에 한 줄 추가합니다.

## 결과 기록 형식

```markdown
## Paper
- Title:
- Link:
- Original code: (있으면)

## Scope
재현한 실험 범위 (예: Table 2의 Llama-3-8B 행만)

## Environment
- GPU:
- Framework / version: (예: TRL 0.x, verl 0.x)
- Base model:
- Seed:

## Results
| Benchmark | Paper | Ours | Δ | Note |
|---|---|---|---|---|
|  |  |  |  |  |

## Discrepancy
수치 차이가 나는 이유에 대한 분석 (하이퍼파라미터, 데이터, 연산량 차이 등)

## How to run
학습, 평가 명령어
```

## 권장 .gitignore 항목

```
checkpoints/
outputs/
wandb/
*.safetensors
*.bin
*.pt
.env
```
