## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:b8be0a0070996f0547538a0cc12f3279c1ca8facad99e89edec041ecb24e9d01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:802d32c28d079db722c57c8b485d65d3c88b431a4f135b334fb1bbd498ab311e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322702532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ac5a148c80ee350626503586b0217503b05cad46d3c17c6861af0f37875a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:06:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:07:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:39 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:39 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:00 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:27 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2506b4ea38e99bf5fce3be308c6532c1a057bf7c5c132bb59bb1b78ccd2b2b`  
		Last Modified: Mon, 26 Jan 2026 22:08:06 GMT  
		Size: 92.4 MB (92433515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606b852e3c333533b6267cbada59c6fbc954cef2b3af5c4c84f2f9bd6ca56999`  
		Last Modified: Mon, 26 Jan 2026 22:07:54 GMT  
		Size: 93.4 MB (93354538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4347221e94b3b802cdf17619e3596573f093ded7ab14c5bf72267ec056da636`  
		Last Modified: Mon, 26 Jan 2026 22:08:03 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cf8bc836937d7b96a844bf088ff10461d6c41bd9f9aa70d45dab8533ef1ff32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d5fc28e5884d1cdcc7104a6c75f9df98eca2b0faa65788daa202f1248f1a42`

```dockerfile
```

-	Layers:
	-	`sha256:c9a1ee01eda1813ef33ab9f702dc9643c90fefde35f73535f259619ebaa0e35c`  
		Last Modified: Mon, 26 Jan 2026 22:08:04 GMT  
		Size: 10.5 MB (10497031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03ebf6d46922b61816210999796d7deda44f4996c1baf129a6c2deebc7b99087`  
		Last Modified: Mon, 26 Jan 2026 22:08:03 GMT  
		Size: 28.4 KB (28384 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:b4683d10d19df6a1c1404b0dddc893b545cb9648e56171a88b3e3763fbbfc689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281608018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4279b9373ab162d2fcdd8676f0a3bca0b09e8afedaab13b6fe65a2965d414d1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:11:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:14:05 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:14:05 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:14:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:14:05 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:14:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:14:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:20 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:03 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783a26e775ff966c330d6249ce357b09662c68cfc4648b460fcef3edd5babe74`  
		Last Modified: Mon, 26 Jan 2026 22:14:32 GMT  
		Size: 66.3 MB (66288761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205fc7a73de56b4f5ea25cad036ec0f33fb7b33229a77437a24f71a2e0db125`  
		Last Modified: Mon, 26 Jan 2026 22:14:20 GMT  
		Size: 89.5 MB (89526761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab0f0e1b54a10de43feae879a3f883a73450e6b84061a3b547a8d45de1c6bf4`  
		Last Modified: Mon, 26 Jan 2026 22:14:30 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e0f539dc707dad26fb05977c9bedaaa88331d4fa9dc115a4f2e2886f85f2088d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a2aa13a17b81cf36fe2ff83a973596618b8cfb94352e2e7c804cd61849e795`

```dockerfile
```

-	Layers:
	-	`sha256:21f2d272fa77334c62f7016629aba9257515afd7be6365ee067286d243b360e1`  
		Last Modified: Mon, 26 Jan 2026 22:14:30 GMT  
		Size: 10.3 MB (10303727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f893509ee7fc1bb33a5a1411ced7f846bf537f6b9bcd6025eb93fe76492b8981`  
		Last Modified: Mon, 26 Jan 2026 22:14:30 GMT  
		Size: 28.5 KB (28496 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d2ff4c5fd19a0828dba21eb40978663075fe4172f5e6500d9d2d65be93470a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311374470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b581ed425def0a5a5b728f60c7df374b8f139e731e0ad10804254f830cb5895`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:07:32 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:07:32 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:07:32 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:07:32 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:07:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:07:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:45 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:05 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eabaa4f393f44fa79aa70e86b329e50da09ab92805bc939a418a997232fa785`  
		Last Modified: Mon, 26 Jan 2026 22:08:02 GMT  
		Size: 86.5 MB (86506707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c3fde52f4a9ce3ba79f004ba1b1e261e66970dc6baaa4a0f9b9bee7c6d5ab5`  
		Last Modified: Mon, 26 Jan 2026 22:07:42 GMT  
		Size: 88.4 MB (88417257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647b0218b6d03bf17013672a3564651545c6aca1dbfa9e1551e3d9fe8b3ec983`  
		Last Modified: Mon, 26 Jan 2026 22:08:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7f99217766061b85c0fea368c09f03ae57079b96cc85d30ca144cf5efed2f51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7603e88efa58183659f0e826b2b36357384457ab75729a32f7b686389ebf5099`

```dockerfile
```

-	Layers:
	-	`sha256:47e18b2abbc5704503fe17ff4ee21e7f3ee868841498ace42ea5369d362b033a`  
		Last Modified: Mon, 26 Jan 2026 22:08:00 GMT  
		Size: 10.5 MB (10524855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad095aa31fa1af741066539f29778983e6883b1d56d9f1056b9a31a65a2903b`  
		Last Modified: Mon, 26 Jan 2026 22:07:59 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:0620164968cbeee96886078ddbeda60678140d8ab3d952bae810bd667fac4305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321871058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7f96ec2fe82dcfebc292a764bc5001c04a6f9c1bf733dbf0dafa7a94e78074`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:02:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:04:55 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:04:55 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:04:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:04:55 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:04:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:04:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ec54d337d067729b748c8f421e417d2e02e79e9e0caf328deaa1b815a93c883`  
		Last Modified: Tue, 13 Jan 2026 00:41:57 GMT  
		Size: 49.5 MB (49468594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ef3b5e8322d4c8e5ca6198e931fb91c384bac3ef8aafd81a71617e9534b7ab`  
		Last Modified: Tue, 13 Jan 2026 02:02:14 GMT  
		Size: 24.9 MB (24871330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be0f262f5ef3547fc45c5726dd33bf707569fc1cceccb9f87c4f4965c4f9ed`  
		Last Modified: Tue, 13 Jan 2026 03:03:36 GMT  
		Size: 66.2 MB (66234261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ad4818337eaeff7cd9ccaa04a6f33469afc92d02e7801215a99ad0c646ee81`  
		Last Modified: Mon, 26 Jan 2026 22:05:24 GMT  
		Size: 89.9 MB (89858990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb24967b184a59692854afa79a294d0d5b0fa84b707a952b78449312c20956e`  
		Last Modified: Mon, 26 Jan 2026 22:04:59 GMT  
		Size: 91.4 MB (91437726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18a6a758f7d5c768b19351746ba3984b1e7439c9a4a6357f72b51c8b65c1e5`  
		Last Modified: Mon, 26 Jan 2026 22:05:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a28bb78d81bc1e81b27553ad0eb2eac86f0853e4f421b516e0d9dc1a0df908fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbbed6f60c744f1f502d7240f50ce9d09f7612f64d007f55b669e3ab44f07a8d`

```dockerfile
```

-	Layers:
	-	`sha256:6a69017abda76e24b0aa130eda7843af1dbb995f4ead785b16ede5d1d6d4a302`  
		Last Modified: Mon, 26 Jan 2026 22:05:22 GMT  
		Size: 10.5 MB (10476611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b92f96345397422c864131f10fc573c7f6f4b29cdad003272cd9aca6c8b13c1c`  
		Last Modified: Mon, 26 Jan 2026 22:05:21 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ca4b06c8dffd652b1c0989e0abc8d6cdad1cec22981d1e5115e0c8df358f47e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292928653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e02326c380adb0743d517dea2ef85d2eb666373da635e79c0bd42d9f7e6deb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 16:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 21:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 22:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 27 Jan 2026 00:00:56 GMT
ENV GOTOOLCHAIN=local
# Tue, 27 Jan 2026 00:00:56 GMT
ENV GOPATH=/go
# Tue, 27 Jan 2026 00:00:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 27 Jan 2026 00:00:56 GMT
COPY /target/ / # buildkit
# Tue, 27 Jan 2026 00:01:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 27 Jan 2026 00:01:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b4c94e33bcdbce9a62a95be51a6e5f8ed2efc653e4be8f8f6722aa13d9d65461`  
		Last Modified: Tue, 13 Jan 2026 00:40:12 GMT  
		Size: 48.8 MB (48763393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3ebdc0d40ea56bd8ca0e23bf6a7db8ca22ab77cacf0ba126e24eb42d35c708`  
		Last Modified: Tue, 13 Jan 2026 16:17:52 GMT  
		Size: 23.6 MB (23614652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ee435e05dd9c53ddee45b81a8f55939374cd926a0e00239c752bb0832a5f8b`  
		Last Modified: Tue, 13 Jan 2026 21:22:59 GMT  
		Size: 63.3 MB (63309962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659edd573efc55ccb964dda4fd8e0b2b02903c5753a704b10ec114e6a6fa5f32`  
		Last Modified: Tue, 13 Jan 2026 22:44:42 GMT  
		Size: 70.0 MB (70021799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9749d62610ee331db926d31c01c64c3877e6fbb53e45e6a795399493a0f0c40c`  
		Last Modified: Tue, 27 Jan 2026 00:03:08 GMT  
		Size: 87.2 MB (87218691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f13b58dfbee233c3207d465ab4acaccf6c6d6c58450bf7c6409cdd1f403ea67`  
		Last Modified: Tue, 27 Jan 2026 00:02:59 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9218318948cde0375313014e9f487ea8bf5b68b8736bb04bc4f525ea7a103b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b964598ab7045ac99fbfd2ef33f5eebe4124d13788c956ae24cdbf1ce42e1ecf`

```dockerfile
```

-	Layers:
	-	`sha256:b00d71212f50cd227a43de941e07f7789830f01e6ba494aa934be854d19f550b`  
		Last Modified: Tue, 27 Jan 2026 00:02:59 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:4f76046c42c97e57af4736c41c8f00e05d5571a79bccb50cab813344add8b059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328323877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e29f7ed114d59fc18d9ebf43741ce71b901eb65807e83144b1eccb023241`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 06:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:34:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:34:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:34:17 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:35:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:35:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2769c4ec4b4d67e8059086401477839f8b9d5a5026dd27df50a3c7ce33b9db`  
		Last Modified: Tue, 13 Jan 2026 03:35:30 GMT  
		Size: 25.7 MB (25670703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5fcb80ea7d84a82ea96c11045a4f40d0943808d5c5334ea90de2f7ed44f4c4`  
		Last Modified: Tue, 13 Jan 2026 06:38:28 GMT  
		Size: 69.8 MB (69846016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f0f633f910365ca19f51f78c2aa5d0bc7016fedac96025836f2d2543eb199e`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 90.4 MB (90428698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3fbdd047cc229947289d64050103b3f46ea0891f972e8e261f84917802eea`  
		Last Modified: Mon, 26 Jan 2026 22:36:06 GMT  
		Size: 90.1 MB (90050925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b6627a639b7e6b71ccda88b19b6692df25da804d22e9903f0664270e0fdae0`  
		Last Modified: Mon, 26 Jan 2026 22:36:02 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:cb671245a62593631605fadd26dd97a863bb68890024bc35bea588d34df38a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d67fb41bf9d3c561e48435dbc7756ef889f641b2a5ef23b575de8c7e641193`

```dockerfile
```

-	Layers:
	-	`sha256:607b5018cfdeafd83bd02e1d54b8d0abc55cb289d462c3d89d8765c93647e701`  
		Last Modified: Mon, 26 Jan 2026 22:36:03 GMT  
		Size: 10.5 MB (10469516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:998f3bf8d752109be3ea37e6df1cae4b344af8ab588d4ce541d679ee276326cc`  
		Last Modified: Mon, 26 Jan 2026 22:36:02 GMT  
		Size: 28.3 KB (28259 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:2619af5469b65bb196b6fa6f07f83ad82ed4c419e799199e9cf2442fafe95c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.3 MB (296299037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de71311c1275e76affe5d708b0bca21f7fefa4bb80a76af2de0c12de902f6e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:09:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:14:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 19:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 26 Jan 2026 22:12:17 GMT
ENV GOTOOLCHAIN=local
# Mon, 26 Jan 2026 22:12:17 GMT
ENV GOPATH=/go
# Mon, 26 Jan 2026 22:12:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:12:17 GMT
COPY /target/ / # buildkit
# Mon, 26 Jan 2026 22:12:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 26 Jan 2026 22:12:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8133db08df54d1100dff2f0259f057251959db22c09d939ae558af001aa8088c`  
		Last Modified: Tue, 13 Jan 2026 02:09:58 GMT  
		Size: 24.0 MB (24032491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb4cc23aeea1b258f198103e8c2d450f82da1d5de8a3eb227ed2969f60d97c4`  
		Last Modified: Tue, 13 Jan 2026 03:15:23 GMT  
		Size: 63.5 MB (63501276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc97fcb15f261da40ae9f478881ed380e217eb71619ee24d8a4cefbaec79cde`  
		Last Modified: Thu, 15 Jan 2026 19:33:09 GMT  
		Size: 69.0 MB (69018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d1ebc1a42fde765fe01b70de439084ec52a344bfa25acb00b6d281dc10102e`  
		Last Modified: Mon, 26 Jan 2026 22:12:55 GMT  
		Size: 92.6 MB (92608018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af765e0c8c439d90401a094e299b2a23483473c20b0dc803b3aff0da389f5cf6`  
		Last Modified: Mon, 26 Jan 2026 22:12:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:75612c2026e71116f79bbb3ff4d7ddacef56f0ffecc58a277d7282aaedf91fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268a601c188a82c3179c499675d65183230dbfa44f305dab1da62f53359b9454`

```dockerfile
```

-	Layers:
	-	`sha256:9c5aca52433d33e6e37473b21f61a617793b6fdc3da6dcf26b2bac92d486fe4b`  
		Last Modified: Mon, 26 Jan 2026 22:12:59 GMT  
		Size: 10.3 MB (10328789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1803e356f55fe7b27f773a87b207ef5a65fa0799ba1ea69b9c4ba29d1fa0274`  
		Last Modified: Mon, 26 Jan 2026 22:12:59 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
