# Modal Pearl Miner

Serverless Pearl mining on Modal.com (H100/A100).

## Quick Start

```bash
pip install modal
modal token set --token-id YOUR_ID --token-secret YOUR_SECRET

# Akoya Pool (H100)
modal deploy akoya_modal.py
nohup modal run akoya_modal.py > akoya.log 2>&1 &

# Pearlhash Pool (A100)
modal deploy pearlhash_modal.py
nohup modal run pearlhash_modal.py > pearlhash.log 2>&1 &
```

## Files

- `akoya_modal.py` — Akoya pool miner (H100, ~600 TH/s)
- `pearlhash_modal.py` — Pearlhash pool miner (A100, ~150 TH/s)

## Wallet

Change `0x6ce2e1f271f98fff5dea2daf4e5b6aed993ceb15` in each script.

## Monitoring

```bash
modal app logs akoya-pearl-miner
modal app logs pearlhash-miner
tail -f akoya.log
```
