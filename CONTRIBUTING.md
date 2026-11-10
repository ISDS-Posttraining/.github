# Contributing

코드 구조나 프레임워크는 편한 대로 쓰고, 아래만 지켜주세요.

1. 레포 이름은 `<method>-repro` (예: `dpo-repro`, `grpo-repro`)
2. README에 결과표 넣기. 원 레포를 fork했으면 `REPRO.md`에
3. 체크포인트, 데이터, wandb 로그, `.env`는 커밋 X. 가중치는 HF에 올리고 링크만
4. 원 저자 코드 가져다 썼으면 출처랑 라이선스 적기
5. private으로 만들고 정리되면 public으로
6. 레포 만들면 [org README](https://github.com/ISDS-Posttraining/.github/blob/main/profile/README.md) 표에 추가

## README 형식

아래 복사해서 쓰면 됩니다.

```markdown
## Paper
- Title:
- Link:
- Original code:

## Scope
어디까지 재현했는지 (예: Table 2, Llama-3-8B만)

## Environment
- GPU:
- Framework / version:
- Base model:
- Seed:

## Results
| Benchmark | Paper | Ours | Δ | Note |
|---|---|---|---|---|
|  |  |  |  |  |

## Discrepancy
수치가 다르면 왜 다른지

## How to run
```

## .gitignore

```
checkpoints/
outputs/
wandb/
*.safetensors
*.bin
*.pt
.env
```
