## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:ce37431244dc0e3af5c5ce275020d1aabe5196769b00e1c538def4eadb3ee336
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

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:2a5788f1ef4c38aed296db9d4ca6cf5f7f6a12677503878908e6964da20cedca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339553174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a310417ebe502cbbe43e5bef80218c88f5bc844366f3fc3a31b45dd3495f1b6d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
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
	-	`sha256:8a1b788db741b54a35963c6f6401884a2829ecd172fb0ea104b6eebcf85d0cdd`  
		Last Modified: Wed, 19 Feb 2025 00:32:22 GMT  
		Size: 86.0 MB (85971522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc5764bfa5625e90d4c9d1c4bb7361ceb8d3451c8f3534f5e3a80e9f8aa6e4`  
		Last Modified: Wed, 19 Feb 2025 03:27:14 GMT  
		Size: 129.5 MB (129532433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179260317451e21c422dafeaf8060dd14b7bbb33c36eb13c5ccc7ea267e69fef`  
		Last Modified: Wed, 19 Feb 2025 00:31:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7406661c19280f1dd19aa17e630b719536678ac3db4745663b03d64d18e36f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0377292e429ac57f20c8769dd7121bcea4bd8341a3de211e7456dab8ea3105`

```dockerfile
```

-	Layers:
	-	`sha256:77ec3909ca9e263f4d1b3c1f7be4718637774c9a48c37579e62a529240b1d7be`  
		Last Modified: Wed, 19 Feb 2025 03:24:34 GMT  
		Size: 10.3 MB (10267086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3a636b564fa97e7c6b4942388606d6ba84adc11dd652eb42755e25b7503dea`  
		Last Modified: Wed, 19 Feb 2025 03:24:35 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:68ed1c3dd696e08a72bb68b38154616ddd3b01b6d96fff51fdef1ecb57ac2a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302029595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca707221a36d73e3cedf95ce974aaa645d123920f4157cfcbd362d7d82c662c7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
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
	-	`sha256:ddbce18d551f744b2f9a445aaedbcd8c5e283783570d9da4735469555773098f`  
		Last Modified: Wed, 19 Feb 2025 01:09:47 GMT  
		Size: 122.8 MB (122798265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf714c2f9c8e71f7fc0357bc7a7b5d441ea1cf1ac4d50d656c2fa5d2b8ece60`  
		Last Modified: Wed, 19 Feb 2025 01:13:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:3a2ec0ff2c49b2bbf05e734ec1e84fe67bd3a8677fbebe8d861b9d3d07891a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10100595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1523cae93e5a1f9b3471a697d251a83708920b5f8b84b985c551fc02fd4c6c4b`

```dockerfile
```

-	Layers:
	-	`sha256:ada491dc9f80a3f4ef15756fd67f2e870ce829981c3942a4f30f1e4d70235ecd`  
		Last Modified: Wed, 19 Feb 2025 03:24:41 GMT  
		Size: 10.1 MB (10073426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4878aaa17422d40af91fa3489bf4b520820a4f2acb04e7b5f7f03eb4a00086`  
		Last Modified: Wed, 19 Feb 2025 03:24:42 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b0b907b2a27ffe2cd7e6cfc3df776c788fd692021248a0f50e8025a280080c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326378121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4e7f884dbda59c21fc126fb3661b53c789046a9630d9c3511427a0ea6ad3ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
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
	-	`sha256:5298385c49d911d309658b69d6f0a6876dfdb4d5bed9f2c1fff825ca2fb2fcdb`  
		Last Modified: Wed, 19 Feb 2025 00:41:18 GMT  
		Size: 122.4 MB (122353292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d905b978651aa6c656ce0dc724a81185ca9f4364e085f45dcb88e2a7dd8ceb`  
		Last Modified: Wed, 19 Feb 2025 00:43:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:fafdd5dd9cc3effb4b8c60cf61e219c61313053879fc2a4b5754a6aaac8ead8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e170f26e1b55572e3234d6a282f4c26e796e99a8cbbee240081b2693f2b3d59`

```dockerfile
```

-	Layers:
	-	`sha256:86b85570b88d716dfd7df720ef6b00cb40df2b55257e770fd9c885ea47c96454`  
		Last Modified: Wed, 19 Feb 2025 03:24:47 GMT  
		Size: 10.3 MB (10268658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4416271fb0f2b4e5b66b45135b9e1de02ab2d52bd2f0203101fcf461984ffb3`  
		Last Modified: Wed, 19 Feb 2025 03:24:48 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:1fd1be8d1f2d2d7d8ecffbad6688930c45513f199c7f3cb66072e2adb3f5f8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340333168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee88e54ac0e4c62f435f644129348e8c17cb58badcaaa7958d1faf0e16313c2f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
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
	-	`sha256:3441c79830350ad8091e1424887dc6507365b0dbe8853e44bbe44ce9cfd8aed7`  
		Last Modified: Wed, 19 Feb 2025 00:32:17 GMT  
		Size: 87.4 MB (87398184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c865367c21802db35d933085cc324482ddcbb8bd28bfbcd89b6ea5d6a248d00d`  
		Last Modified: Wed, 19 Feb 2025 00:32:09 GMT  
		Size: 126.2 MB (126166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98332cfaf7fa4100933106c0a98da2bb33be1a5970596615bb289e4ddcc95ca`  
		Last Modified: Wed, 19 Feb 2025 00:32:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:6f0f85f2e9ce5d46898aa8b5e943881e9dab92187a1aec9e92927645c9dacde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba67f02b99c65a857e0e167b7aaf6fec42f09e9130bf3926e195afaef3c0dfb`

```dockerfile
```

-	Layers:
	-	`sha256:c2e2431f2321f52a3af4aca784b685d37fff509c7ee276829b545bb34fe3e1a6`  
		Last Modified: Wed, 19 Feb 2025 03:24:53 GMT  
		Size: 10.3 MB (10256877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65251fd6fb7e96418207cda1e436e8ab61590af33453adc39985888a4c585d7d`  
		Last Modified: Wed, 19 Feb 2025 03:24:54 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
