## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:65e70c9633830f31b391d983000de748c0637e64ade0c7f577c76ad15071ec66
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
$ docker pull golang@sha256:9cad8121c302b3da14b40d56b6ba7811508c7f2528626d7935476f8bcb89326d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312355182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5656ddb6af1c1890935650a12ba6825229d75cba8f7e45aa5d9d0bd2016892a6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbf972c6c2f5b7313ae3cb74e63888ab70931bcd9aefd960f9a38c540dbf2ca`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 24.0 MB (24020692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900e2c02f17f686733f4f957ddfb07b3342d1957d87b56254634d4fbb2abb81d`  
		Last Modified: Tue, 01 Jul 2025 04:11:56 GMT  
		Size: 64.4 MB (64399879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab3f40657c14d36fe38af71fb641e89f8f481e2530a1bba2e1ae92891a2e30`  
		Last Modified: Tue, 01 Jul 2025 05:15:15 GMT  
		Size: 92.4 MB (92355114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8f8c49f445d30fa7cd4c028a18d5365e5bdfe97436ef61eb7709425c99cad`  
		Last Modified: Mon, 30 Jun 2025 17:30:36 GMT  
		Size: 83.1 MB (83085055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433d0f7635c87746eb977ce85bff9ba6c0c51fc62ba7086683965601c101308`  
		Last Modified: Tue, 01 Jul 2025 05:15:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:bb12deddde0e75c7283f227ef24e3669694254da3c2bf9d711f1c401cb2707f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10516404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d74b837d614ee3c1597415aebb4fbbc23cc71b5b16a097fd206535e31508bd0`

```dockerfile
```

-	Layers:
	-	`sha256:d3cebda2fc30dd0b113aa063990c76850e488d08fa8f80f3fa76975fe30ac9e3`  
		Last Modified: Tue, 01 Jul 2025 08:23:40 GMT  
		Size: 10.5 MB (10488745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aabf8922bad263300698b71f071dda8977eab4b1430069ed84ca21cb53c5a2`  
		Last Modified: Tue, 01 Jul 2025 08:23:40 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:05b197c810639636e83d94bad85c75b3821b263201c004661cdd18817f0d2b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272161678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10952d6e2b3deb6b04214a922eb1ac7c710638fee92d6e8daa1ba5ef4105aa03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0a248bc7fbf888bccbf6729078aec3b1f376d1d95c8ee77854eaa13fe0986`  
		Last Modified: Wed, 11 Jun 2025 18:27:12 GMT  
		Size: 66.2 MB (66208380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6586f6a3b72edca5355ba2231baded357cf799f55b8944edc8ae75b0c7b67acf`  
		Last Modified: Mon, 30 Jun 2025 17:31:46 GMT  
		Size: 80.2 MB (80163369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338ac6df1d23b684cda5d56ae4db81602f850a271ef7637e49ffc0c19b8764f9`  
		Last Modified: Mon, 30 Jun 2025 17:31:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:67ad50b13fc71d798faa1b7d9c03d4cb24385b2d43d070f5dae744c89cc66513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f259e7bbf4f3e48097884acb056c2ebb0bd27907c9abb43b05a096fb20bf0c0`

```dockerfile
```

-	Layers:
	-	`sha256:50ffcca7b570220c58734a0cf57fa001d110f6f6c97f9ff02a06e94904d55009`  
		Last Modified: Mon, 30 Jun 2025 20:24:06 GMT  
		Size: 10.3 MB (10294103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef21ee5ddf7dad8aa470fbff7deed36fcca59da8d14aa4438c8f2660aa8e0f4`  
		Last Modified: Mon, 30 Jun 2025 20:24:07 GMT  
		Size: 27.8 KB (27783 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:913eb64f1ad3974fcd90dd8a0eb7ac16dd6bc46928fd0ab4b6f5631af8a72117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301736543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a76bc805b37b95a2c038105fb38700faf9c4bda10e2f18363d56bcc2b05d147`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399a17febfc3c309501dc6427821a98f0a207b994da4369bc17d53bfee0ec1e7`  
		Last Modified: Wed, 11 Jun 2025 23:08:08 GMT  
		Size: 86.4 MB (86425354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f0e5c856fb20135c901f955406b40129ab946b3615cd5e0d5839e969930423`  
		Last Modified: Mon, 30 Jun 2025 17:34:31 GMT  
		Size: 79.1 MB (79057770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa7ae73b1571a3c9e89d3c8f013d261e1a8e4bd4b7d6e54062017e2f991bab0`  
		Last Modified: Mon, 30 Jun 2025 17:34:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0acbf1afd18a5ffcc426db8e7a3102845757c0472a94a8808359179c6c7c36ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d1dc4b36ae7e870449a70c18d5110ee1cf7e48e0030f40f80a5397cbfd158a`

```dockerfile
```

-	Layers:
	-	`sha256:d95cf68c3de8cd1580dce87b0ff3069a95b731f1b286dfe0a114e644777a695e`  
		Last Modified: Mon, 30 Jun 2025 20:24:14 GMT  
		Size: 10.5 MB (10515237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b8de2816276074e6e117b46bcc225fde34442f2f114668607d751480894cb90`  
		Last Modified: Mon, 30 Jun 2025 20:24:15 GMT  
		Size: 27.8 KB (27817 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:251f7708a4006544815a50d1af3bdd9780ba6f11eb6f2e16e855b3b337f2b87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312144444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39338d54d792c26aa4acfdb2188a0d13f2cafba774f9123e1891f83b64eafd3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cda39ccb3b2c2ec24c975a682bdeefbed3c8426fce31590d9640d34689c0070`  
		Last Modified: Tue, 01 Jul 2025 05:15:22 GMT  
		Size: 89.8 MB (89774474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2781a7c01ceed520d1e8478386c7e0683cbeab9ca6a32207c24229a367897`  
		Last Modified: Mon, 30 Jun 2025 17:31:11 GMT  
		Size: 81.8 MB (81810142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19dc0589072236251b7f8722d216a29c41254b3206868a9a0e543fa8c40250b`  
		Last Modified: Tue, 01 Jul 2025 05:15:16 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:80f6824130f458d1546222c88dc9df09fa235bed29693ab58d12fc9ea4852dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10495938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1d7b890b4f8b9e17e57e8c7043f5f69acb81fcd02bea32af26b0ab5683982e`

```dockerfile
```

-	Layers:
	-	`sha256:ac48b03f4ef0757b6393a1a957ad5153b34bdc86e64daf27075e006057d7e156`  
		Last Modified: Tue, 01 Jul 2025 08:24:00 GMT  
		Size: 10.5 MB (10468323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:619141567b26d5a148525e8bdc61d51f8d920b65b726df4671ac0a325d254578`  
		Last Modified: Tue, 01 Jul 2025 08:24:01 GMT  
		Size: 27.6 KB (27615 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:443a8904b2e3e3531c585b02d2d4c77be78160c1760565c3bb7e95b91383a347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283441108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2111ce3dece0c18ab7fb704b938060d0aea88f22fc6a17220779544d2cc1f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8492b77d6bf957cded76e087bd45cb2dc99a21e61d8bf5a9dc72814542a2ff45`  
		Last Modified: Thu, 12 Jun 2025 08:23:42 GMT  
		Size: 69.9 MB (69945632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93da9c44ad0cf5204fa695dbbb19af7842d91e70bc8e38610b3cca4f51ff75`  
		Last Modified: Mon, 30 Jun 2025 17:56:24 GMT  
		Size: 77.8 MB (77812415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1507d7eb57d50b3e84d7d8d884b473f49ed7a1cb2c1f0dadcca21295ffb2e8c9`  
		Last Modified: Mon, 30 Jun 2025 17:56:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9506d612f2d1e4ffb1627fd23437a04a4ea593582a4e2a07b06e8c401a39b87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c417adeecf8d2d15c76e924baf64f173658fc1357ece72df87eeaa00b86c76a`

```dockerfile
```

-	Layers:
	-	`sha256:22188f1d9cc63dc8901ce67f40b066dcab18a52dc09b8d7fb61d2be3cf9c50d4`  
		Last Modified: Mon, 30 Jun 2025 20:24:30 GMT  
		Size: 27.5 KB (27531 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:b1db25e151e9a9b478703c939da46b5a8f107ed9d34f3fe3eb8fd8ab6c382850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318554846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7432d66ab8d3779d9e1979c050d311044a28a6b1a675ee820dc68edab1c0e02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04a97584b773cb2e3f5ef36cf5fd266e7a5329383a4acadeef6edef21349bf`  
		Last Modified: Wed, 11 Jun 2025 23:31:25 GMT  
		Size: 90.4 MB (90369172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90415633da1367f6a55f0b20986162d53698245a02ffb8afb2ac26988cca44e`  
		Last Modified: Mon, 30 Jun 2025 17:31:50 GMT  
		Size: 80.4 MB (80351038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53a85ee12f80b15b0be43515ddd328030c56eec08d3a8edc27419c785c319f`  
		Last Modified: Mon, 30 Jun 2025 17:31:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a19e1e440da571d1df33f1c2399555a3bea8812b6858fcdb93479d1f8f22c32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddf85be01be04754e32cb43e18c674f43a71e087185f9d627ce45d8a7a44b54`

```dockerfile
```

-	Layers:
	-	`sha256:99d02b92a9d9845e747aa835af16f981edd8250937136aedbbd11641e1131e84`  
		Last Modified: Mon, 30 Jun 2025 20:24:35 GMT  
		Size: 10.5 MB (10459872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f141d16ea946a9ccac4293c8bf3bf48602c3192568a490d96555a1f20ebf1eb1`  
		Last Modified: Mon, 30 Jun 2025 20:24:36 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:c7d282ceca390946f29ce3d34d4114a0c6c72d5f91ebdb96c6318a14c5dab640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285221407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1968892f65de76770f5247d5b66a738f09305a61c84e7b7bfef4c07d247de929`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dca9cef3741351ad228dc4986e66f3e324bfb88d5cc9e2b190dd3a3abf7dcf`  
		Last Modified: Tue, 01 Jul 2025 05:30:26 GMT  
		Size: 24.0 MB (24020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff1e32b479a11528098c70ba4af6292099abafcb29e0823d2861c86032c9b0b`  
		Last Modified: Tue, 01 Jul 2025 13:41:28 GMT  
		Size: 63.5 MB (63497964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cae47c11c46102ab7ff9335e654c0977270faf61319eed0a1a51e7f85f25cd0`  
		Last Modified: Tue, 01 Jul 2025 11:37:27 GMT  
		Size: 69.0 MB (68958019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1d310562389511c34710f540a5f40a96841fcdf844e9a2742b152e861d58d`  
		Last Modified: Mon, 30 Jun 2025 17:32:00 GMT  
		Size: 81.6 MB (81595438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a506c69d133fb5820ce707d709ca47f4a1df3905928d027b193b8cdb54364668`  
		Last Modified: Tue, 01 Jul 2025 17:29:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1f53cc63f53c4486e49b1aed86d2523d2630902eb08c27332f0f9280c912c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10348162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f7614067c244df155e005fcaf1c77725fc17670cecac426b8499a2869275e`

```dockerfile
```

-	Layers:
	-	`sha256:474d47379758bfec5bc355b3f4c7654e2cfe4e310c70efcd6377734da7e34e46`  
		Last Modified: Tue, 01 Jul 2025 20:24:56 GMT  
		Size: 10.3 MB (10320503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:838ecdfa976ef4b7243aa3fbe96227caa2eb9814967615e603ea89ab40db5562`  
		Last Modified: Tue, 01 Jul 2025 20:24:56 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json
