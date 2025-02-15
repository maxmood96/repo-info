## `golang:tip-20250209-bullseye`

```console
$ docker pull golang@sha256:6b19682cad570ed27505725540885526b82407e1806e6534b1b07dc48fbae329
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20250209-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:1180c0e7f7cdd28bba4e44e8426d90a0835787275f1e535d0d9b029041850878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339237509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eacbf9fbac22d7e5532459b50384f4e0e04690cedd9fca681ce27f28c8afdc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0388f0d5bf1adc15e551cceee5a85f21b1ebf5b13c380ee0e941c5d55013598`  
		Last Modified: Tue, 04 Feb 2025 08:47:02 GMT  
		Size: 15.6 MB (15558271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d473f760e53d3d50afd1cebc7113387023a04ff8ec34073c4412b465ccc2fc5`  
		Last Modified: Tue, 04 Feb 2025 09:04:02 GMT  
		Size: 54.8 MB (54751917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac1e880ac4262e770b5ee1b650408d9e84a0e6d2c3bdf9c7a04145be483029d`  
		Last Modified: Sat, 15 Feb 2025 03:39:46 GMT  
		Size: 86.0 MB (85971755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f767e601eda3139d3a2c86388748ee052ac66ea4515fdb8e54673dc9e44217`  
		Last Modified: Sat, 15 Feb 2025 03:10:47 GMT  
		Size: 129.2 MB (129216535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a314e8948e2c109faf84065014a3ba9c99704683923f935c4463b366a7f99ddc`  
		Last Modified: Sat, 15 Feb 2025 03:39:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250209-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:21ed9b8666dbf091d25a850e35ca95757c55cbeadff583150c345244d33a5775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1b085194a092b8a19f361d4d24181e640aecda31920fac65971ff6b0d679d5`

```dockerfile
```

-	Layers:
	-	`sha256:fc1eaab41313d71e63991e05ad8f9b1a898b479a286a21189534162780a8d6d9`  
		Last Modified: Sat, 15 Feb 2025 03:23:43 GMT  
		Size: 10.3 MB (10267086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f26d54c740cc34dccc496d06a932cc0e9e11f9936b91fde72927c62baa20ab`  
		Last Modified: Sat, 15 Feb 2025 03:23:43 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250209-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:2d1756931d4f77c7da86b09d1d2deb6c8d36592807333160838e82c80e89490f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301748049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3fa5f9ce7a81b0a4c845685f46bb0e767fc4e9399eebea3c275e788ce35c611`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 04:34:07 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe1cf520a5741b594ed015a44e9386892026b5310b613c2207dbb1073919e7`  
		Last Modified: Wed, 05 Feb 2025 10:42:12 GMT  
		Size: 14.7 MB (14673818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7c48b43b3adcfcfb794cc307d61fbdfd95ebf9cf80b1a014e90a497356d90`  
		Last Modified: Wed, 05 Feb 2025 08:37:42 GMT  
		Size: 50.6 MB (50640069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939d641c4fb5f7d6edca115cf3c6db8bc11e32ec83c49422dab7839f4914e1a2`  
		Last Modified: Wed, 05 Feb 2025 13:21:41 GMT  
		Size: 64.9 MB (64892491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bce9909702d68cbcaa8d6736165483e5a988ace20a7429491fd9459c92058c4`  
		Last Modified: Sat, 15 Feb 2025 13:09:03 GMT  
		Size: 122.5 MB (122516719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd73a629a4586e96b1bcada0c423b6548eb365c5cf55530fa33630f2ea504e48`  
		Last Modified: Sat, 15 Feb 2025 12:35:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250209-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e7a5e6ed1f9e06cbc18b36133a661a42281dd71e31630063120a8899aae0f2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10100595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efeb2a830d57fd379ed88f259f8056815f027fa7b111bef4df61244879e0e41`

```dockerfile
```

-	Layers:
	-	`sha256:f4e8ed0acc115b8e23d3c9d25b16d49c785fcfd2a2795a614e925061afb8abb4`  
		Last Modified: Sat, 15 Feb 2025 15:23:46 GMT  
		Size: 10.1 MB (10073426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f6a19987c61b807afa64fb61998b1b280e7eeaef3d58b79eb95e35f4dd8221`  
		Last Modified: Sat, 15 Feb 2025 15:23:46 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250209-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5410bd9a5951994fb55724b9a9f7bb939aa97d31975aa8e4626ff0f7db2751dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.9 MB (326883745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf384c19ef2743616343c37ea3beae0d4be66e39751d914037f69dc89acf1df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c7afb1aa0f9672a06c4c7eaa6b7c7e111a91a8d45272dce1e361ac0b0ed79a`  
		Last Modified: Wed, 05 Feb 2025 03:24:45 GMT  
		Size: 15.5 MB (15544055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8e2f45c7ddf8cc116eeb2ac1ef8be70e3639a883c6d9e5eaf1f2dd702dbf92`  
		Last Modified: Wed, 05 Feb 2025 04:03:49 GMT  
		Size: 54.9 MB (54852696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645f8f0990a7270606266e36ae54950c498997c10e31242c830d3106f5fd7ed4`  
		Last Modified: Wed, 05 Feb 2025 03:24:52 GMT  
		Size: 81.4 MB (81382226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905748308911592ab8dd35e81623d80a35a86c1f573f4146926a93bafbba078d`  
		Last Modified: Sat, 15 Feb 2025 09:11:49 GMT  
		Size: 122.9 MB (122858916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5bee105d6facc3a7bdc2a936af8183e4f9c869c039c8b33a343f8a1cebec53`  
		Last Modified: Sat, 15 Feb 2025 10:18:14 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250209-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:fd89c13c8b3664f5e68bc29af4d532f7d31123e2df74f4353deb4e3d68c561f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef5474b3eb048e70d7dcabbbfdb7a3e4f2eb5be0e9734a04dfd867c240f14fa`

```dockerfile
```

-	Layers:
	-	`sha256:e3eb0d70a20021295ecd384aa1d17f72eea849fa09b087d55d71611634ecd128`  
		Last Modified: Sat, 15 Feb 2025 09:23:44 GMT  
		Size: 10.3 MB (10268658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14de0df3bbda9cb81a3782770bf740ff8f0a4a9130bfab91d4b391d047ab0897`  
		Last Modified: Sat, 15 Feb 2025 09:23:44 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250209-bullseye` - linux; 386

```console
$ docker pull golang@sha256:b4ecd4a8208df840e988c91548e2876ed495508aa01715ef522f1d39de90a661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (340038815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa18d85860b2c76acace45df6933e7d76bc2d1c7cbe827482f899cd4ab34f672`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOTOOLCHAIN=local
# Thu, 13 Feb 2025 00:08:35 GMT
ENV GOPATH=/go
# Thu, 13 Feb 2025 00:08:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Feb 2025 00:08:35 GMT
COPY /target/ / # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 13 Feb 2025 00:08:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 05:01:41 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d372eab1872f98afed1da2c899af883a0b3a6e52e25e2690ed35b3d6f859e5`  
		Last Modified: Tue, 04 Feb 2025 10:05:13 GMT  
		Size: 16.1 MB (16062054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4520e7fd9b17628990db3e961c2d7570421849af1fe255937c0a9e48cf49a48f`  
		Last Modified: Tue, 04 Feb 2025 22:03:52 GMT  
		Size: 56.0 MB (56029876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963712fa0dd1a90ffb6870292b18b942f0e2af189f276f807c9c784ebb52e548`  
		Last Modified: Sat, 15 Feb 2025 03:46:30 GMT  
		Size: 87.4 MB (87397951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b2ede4bc0ff1c223f32b8ba810862b4e27669e273d5c1e6c5993b5698ec335`  
		Last Modified: Sat, 15 Feb 2025 03:10:29 GMT  
		Size: 125.9 MB (125872820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5378bb5c3e258d29e009a1eefce158ab51099ab7ec88ad1e4595d30a6877a7ea`  
		Last Modified: Sat, 15 Feb 2025 03:46:21 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250209-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0af4a618497d1bbd04976198d8cbcd31400488e6796a32ef76b63c1c6a458455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846dd9d9357539e6d4d779d75b7a70f9b3a47b5d0af0c2216356450b19b92c5b`

```dockerfile
```

-	Layers:
	-	`sha256:893ee86e09c99440684f4ad6a9e8b00c1a977c97403c213a63978b338fc019db`  
		Last Modified: Sat, 15 Feb 2025 03:23:48 GMT  
		Size: 10.3 MB (10256877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cee0f5fce9ab6746052fb42381d1273f4609bebea3300379e82132413e9a5677`  
		Last Modified: Sat, 15 Feb 2025 03:23:49 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
