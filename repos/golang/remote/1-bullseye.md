## `golang:1-bullseye`

```console
$ docker pull golang@sha256:bc4e42863caac6daf5009fa416f1f520682feb2107948a74f11c2c5fd25944b0
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:d96fd49e85edbd3af56861a86b92c49fa3cfce1105105b7376b5770ac6251714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.1 MB (284070176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc33dda69539a0e04c4083c85a6406c2421a7a1efe0559a0c5e557e35f5ca84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df16681c019573e3211da3a69493c28abc41e22e0cfaaf006fa4e8a20965295`  
		Last Modified: Tue, 14 Jan 2025 02:33:08 GMT  
		Size: 15.6 MB (15558362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d363a1dd2d1714709c84ac8d050f51e921efc51885c202b336cc24f61e3186`  
		Last Modified: Tue, 14 Jan 2025 03:18:11 GMT  
		Size: 54.8 MB (54753534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc5463354de3a5ef31fafc2d5b781a95d3d45211f7997b470b3122564913430`  
		Last Modified: Tue, 14 Jan 2025 20:33:36 GMT  
		Size: 86.0 MB (85971510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f05ace1117d62b655e04f6f73c83617e3e0febc38681dbedf58f477dd0658c`  
		Last Modified: Tue, 03 Dec 2024 22:28:52 GMT  
		Size: 74.0 MB (74047449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2617297b2b1eb97c088e3e3a8b249f86ac6c910bc72cf0e6f6cb0550306df69b`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:4240d24f6e21520f0655c99e9addae27045b8709dbab07eb995c2f29400e5702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41efe34da5cad1506ed62d44224e7a7070122759df3375fef8350a305fcb155`

```dockerfile
```

-	Layers:
	-	`sha256:9523c8d29742709ee91976f1be07d337daaf4dcf4e4955f97cbdddcc3804caf8`  
		Last Modified: Tue, 14 Jan 2025 04:16:21 GMT  
		Size: 10.3 MB (10268941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ecf97428ece1a5e1f3b2259f8ed6a68d6364c0562aac4e9d3a868af1a89979`  
		Last Modified: Tue, 14 Jan 2025 04:16:21 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:5da3888a264e9f2f4b2fb4d5fbd967f01bc71008b7cc1fe74bc76ade66edb1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251430584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e788e85dabf41ad9d5a290f28e35c4d8e4a3367f66414eae71a5b46decfd6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8952ce7729acf39e69f2b455449e7a6e0c33737d28e220354096042bf33230f3`  
		Last Modified: Tue, 24 Dec 2024 21:34:11 GMT  
		Size: 49.0 MB (49024766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42910d07c1ff6fab4a63b5aee5a5925989edf977378fda85da04a7fbf04644d9`  
		Last Modified: Wed, 25 Dec 2024 03:44:15 GMT  
		Size: 14.7 MB (14673838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c52726a3c7d274c95228f4ad5ea84a935ec4fec8334ece90f30c21442894fb`  
		Last Modified: Wed, 25 Dec 2024 13:01:49 GMT  
		Size: 50.6 MB (50640814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eadfed42e09f6eb3598b4c56830560de0b8ae92a44f700c43ed6152228a64fa`  
		Last Modified: Thu, 26 Dec 2024 01:05:03 GMT  
		Size: 64.9 MB (64892566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30004a6a0d94684e60c07bbc44989294b76634fe7cc182dfb2140b1e8c877d`  
		Last Modified: Wed, 04 Dec 2024 07:17:17 GMT  
		Size: 72.2 MB (72198441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904cade93c77fbfab96d157b96bbc844c3d347466d522a4cb3d8e121251c4f7a`  
		Last Modified: Thu, 26 Dec 2024 01:40:59 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:eba46c4718547c11701f831bed7070aa57e0af9826b8eda74ea65bddfdc2fc93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10101871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703787b0760043d863588b4f8ebe35f8b2fd09c44a8ba42c52f795e9cbcc0c43`

```dockerfile
```

-	Layers:
	-	`sha256:db8231904cfbe0a3fbf689d2193a6d9731728bf71b3f46acb8af1915befc639d`  
		Last Modified: Wed, 25 Dec 2024 23:53:17 GMT  
		Size: 10.1 MB (10075301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d0f2051d76716ff4aefc81b84acee336370589e493435b25d3805276f9bdb15`  
		Last Modified: Wed, 25 Dec 2024 15:57:05 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ed84b23fe004edf2efd321117a36136f22017b2f7ea05d2f5752ddb6b9015d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274698134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7ce3fe39169431bd762d7c7d6955da161f78a3eff1580670db6a44f11fc776`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eceb2e49ad0ea75b24fca7d94b98a8202f70828ce20fd23846a542d8dca2667d`  
		Last Modified: Wed, 25 Dec 2024 01:49:44 GMT  
		Size: 15.5 MB (15544017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f980dd00d0ffb99c81471a2f1d6dbe4936d0d24b2e81f9be4ad52c0cc28b66`  
		Last Modified: Wed, 25 Dec 2024 08:12:36 GMT  
		Size: 54.9 MB (54852432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c90fd2166cd71f8a1d227fc6a8152c8111afc492106df95bee104814552f197`  
		Last Modified: Wed, 25 Dec 2024 11:26:32 GMT  
		Size: 81.4 MB (81382412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8f326b04424eb2027d1f0e3255fe568d71a5567f894a08cd86605ebe51c58`  
		Last Modified: Wed, 04 Dec 2024 01:41:07 GMT  
		Size: 70.7 MB (70673417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca9d7faa5c83ba7288ca29f45e8e2ae413f7932ebf5cd15d708bf8882ce6af3`  
		Last Modified: Wed, 25 Dec 2024 15:24:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5eb64bef9b947c67ef0e91f432cc8e5ebf0b416a14fead024a89a2d7d49cd7dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10297139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fb736683f5badae1470ab5cb9cd61300da6da1a3c260ce5f55de6a563d317b`

```dockerfile
```

-	Layers:
	-	`sha256:19b68e8c99e6dde3f235d71f693f86708e7f1858896597bfe8ff35e0cd577886`  
		Last Modified: Wed, 25 Dec 2024 11:27:49 GMT  
		Size: 10.3 MB (10270537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c7e3994ebc03edf738fbc7667dc5f2fb724190db8b04049a16830029b4cb63`  
		Last Modified: Wed, 25 Dec 2024 11:27:48 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:0f136c11209dea15b39eb24c86f7782a09378b2ca3f775862cc590c08239854b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286076741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19caf559a01743bd095b3844fca373854c2f5d6a568188fbc32b4806ddfe9c64`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Dec 2024 19:01:46 GMT
ENV GOPATH=/go
# Tue, 03 Dec 2024 19:01:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 19:01:46 GMT
COPY /target/ / # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 03 Dec 2024 19:01:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b72c0b254e0d45985d121f47650a88f2ee35fbb4ff596c396ee98094e0a26d1b`  
		Last Modified: Tue, 14 Jan 2025 01:33:19 GMT  
		Size: 54.7 MB (54676276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d0c381a5fdef1263d351e698c4afefeb15eebaa7c61c01a804b75362d039c4`  
		Last Modified: Tue, 14 Jan 2025 02:17:16 GMT  
		Size: 16.1 MB (16061977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b411024e8ae7dadedef448d7486b9035f3faedd43c62d2f773ed5d8f87362be0`  
		Last Modified: Tue, 14 Jan 2025 03:18:01 GMT  
		Size: 56.0 MB (56027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469bf4d3f39cf18ecc9b59420baff6347d0ab8f37effd2d38dd92b9de1e383e7`  
		Last Modified: Tue, 14 Jan 2025 04:16:49 GMT  
		Size: 87.4 MB (87398064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253ee978a239d9a54a2ed89c291f3c5c0ee5f67c1dc8c9ff24b239116398d826`  
		Last Modified: Tue, 03 Dec 2024 22:28:50 GMT  
		Size: 71.9 MB (71913121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0170b52f69868d0976756a0f0c675b4d703faec5dbc8216ee24b0fc3fb154df`  
		Last Modified: Tue, 14 Jan 2025 04:16:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:5471093ad3f5a30e4d6d0b1908abfeb77c2a63ba1389bdf11a5c455dba30b136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10285158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7d2bd76f568c05c54ca38ec8c3f2fe9cbe063893c8a65c6fde93901a30dd0`

```dockerfile
```

-	Layers:
	-	`sha256:948d4486a2d28bea2c950fcaf11d24bad8bfe76147ebbb5cd53acb880d4c5fee`  
		Last Modified: Tue, 14 Jan 2025 04:16:47 GMT  
		Size: 10.3 MB (10258726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9acacfbc127d2f373e4106aa8d06628a8ec0053cfc1c7c3ba2f0ebd83f37284`  
		Last Modified: Tue, 14 Jan 2025 04:16:46 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json
