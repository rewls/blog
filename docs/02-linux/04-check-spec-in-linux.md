---
layout: default
title: Check Specifications in Linux
parent: Linux
nav_order: 4
---

# Check Specifications in Linux
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## IP 확인

```
curl ifconfig.me
```

## CPU

```
cat /proc/cpuinfo | grep "physical id" | sort | uniq | wc -l
```

- 장착된 CPU 개수

```
cat /proc/cpuinfo
```

```
lscpu
```

### CPU model

```
cat /proc/cpuinfo | grep "model name" | uniq
```

- model name 출력

### Architecture

```
arch
```

```
lscpu | grep "Arch"
```

### Core

```
cat /proc/cpuinfo | grep "cpu cores" | sort | uniq
```

- 각 CPU에 할당된 코어 개수 목록

### Thread

```
cat /proc/cpuinfo | grep "siblings" | sort | uniq
```

- 각 CPU에 할당된 쓰레드 수

## Memory

```
cat /proc/meminfo
```

- 메모리 전체 정보 출력

```
free -h
```

- 메모리 정보 일부

- `h` : human readable output

## Disk

```
df . -h
```

- 논리 디스크 현재 위치한 파티션 정보 일부

- `h` : human readable output

## Graphic card

```
lspci | grep -i VGA
```

## Linux distribution

```
cat /etc/*release
```
