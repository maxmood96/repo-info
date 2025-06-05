## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:9c3b3ab95db149db75e2a5222f7cc61570c29b89292e44ddb974ca54e0b9c2ab
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
$ docker pull golang@sha256:44d736660c00733808d43cd212987bdf762cfc838ca003160b4ab5b839ecbf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342557285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacbd445229375824acba4354c49b9fb8a650faee96db410a93c24c0483a680d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1da07ef0629447d217e4a27d47e8c139c1025783d4c73fcf6a29fd570f6414`  
		Last Modified: Thu, 05 Jun 2025 21:07:39 GMT  
		Size: 91.7 MB (91729177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c772e4d16fa9b2fa9b4ea3dee2c356c3597d08d324bfd3a1c2b9b5a987e5a2`  
		Last Modified: Tue, 03 Jun 2025 13:54:37 GMT  
		Size: 126.6 MB (126555573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e32026e0d151eca7759a7e53b4aa08c0bd19508d8bcec8d7f5ebad86e651e0`  
		Last Modified: Thu, 05 Jun 2025 20:06:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d4b3bdbb9cda27da07500969de5da21897bd21160e9705554bc226b1933b8402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10342120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78dd2856d124cc37a27a146fc40b1ef414011faa2bf66af6403044182200490b`

```dockerfile
```

-	Layers:
	-	`sha256:407fc083b533817941a905dc5360c696831d7bff2dc5886d0611c480380a09cf`  
		Last Modified: Thu, 05 Jun 2025 20:27:13 GMT  
		Size: 10.3 MB (10315059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab07212a81f83e03e3b75ed1e11224b5ea98022352951001e2dc4b8e568bf4ca`  
		Last Modified: Thu, 05 Jun 2025 20:27:14 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:fbe50c7b96f40eb89ef0b6c631cc0f467bd207e76fea02c9ed5daf29b921c3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300903403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be8130de4a9372c93754290ee41c5b5335489f07fd5b308b1c3c615fc59ed12`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933c7aef3dae867caad0cbafef5672fb39317c04b3bf8bff0868bf265098c4de`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 14.9 MB (14880519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0144e65734487c61a592b9ecd7d576c77bc270bd5d65049de36718f77416c6`  
		Last Modified: Tue, 03 Jun 2025 14:32:58 GMT  
		Size: 50.6 MB (50631322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd4739ceb6e38b56a017a3579cc385de56e1cf7fc98c2c4b4dabd966a9c123d`  
		Last Modified: Tue, 03 Jun 2025 20:02:27 GMT  
		Size: 64.9 MB (64942454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaef207e52620490d9796ba5bb1c39803d44a66aaefee2acfd8d44ca0dc7d0b`  
		Last Modified: Tue, 03 Jun 2025 19:04:11 GMT  
		Size: 121.4 MB (121406962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6d64d050d0750e8cae248210d987e7f57b03057c661b557556fef605eab4cb`  
		Last Modified: Tue, 03 Jun 2025 14:13:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d8d939dbfdea9eaa71e3bef3cba3ef4c5000f984bcc49f28c8b86d61bea267f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10146167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d8ea1da5de4cf38dfa5ebafdea1c900aa15f9ec18d92eb5891a7a1541d24e6`

```dockerfile
```

-	Layers:
	-	`sha256:872d21e0f47877652fed0954e6e9bc6b7da3fb3b210b9158bddd45d0ed709b11`  
		Last Modified: Wed, 04 Jun 2025 01:37:59 GMT  
		Size: 10.1 MB (10118998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9cb03d4611f3c05ec3b50d9804e43338fff5bb6311395805228559fb283c1d`  
		Last Modified: Wed, 04 Jun 2025 01:37:59 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:412f2a6583e81b3a486205e99b783950bb05a34561c71dff4900d2f52e7e7a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328526915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aededde064b6dab15f27f7576e4ae5839b3cfb2532186dc907161d61aea48cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a602f78cf8d696db9521d18affb7ecdb79ff690533efae26e3bdb1544cb1752`  
		Last Modified: Tue, 03 Jun 2025 13:31:09 GMT  
		Size: 15.8 MB (15750382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c1b27af19f7550ac0d9c38bf6bcf26ba7eb53984e7e5e0886342816133c76e`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 54.9 MB (54853236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa4f13c9f2ba35edbb5cc356335d05db12609ba76252d1006e9168557548c91`  
		Last Modified: Tue, 03 Jun 2025 13:56:16 GMT  
		Size: 86.4 MB (86354667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c61459497fa2e2873d988523a87fbbab1017c75b44162e22c190b9fbc0f92`  
		Last Modified: Tue, 03 Jun 2025 13:56:11 GMT  
		Size: 119.3 MB (119320718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd0294bf30750c0f12303010c80c951cf3b582be88fbc7eccd43018117951f8`  
		Last Modified: Tue, 03 Jun 2025 13:56:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:e1bc3ab8f39fd84a5dc08e05d87f7a0ff41e5f76dae3a7d9535bd0448b5ea10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10343537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34feddf7735fa8bbe057a0cee6d617a28a67172f0e7273dd7f807da9c9b71cdf`

```dockerfile
```

-	Layers:
	-	`sha256:e4ec03586c7187ac3eab6a246ee56829a62bbad95c3e12dcb246c0586b11d951`  
		Last Modified: Thu, 05 Jun 2025 20:27:29 GMT  
		Size: 10.3 MB (10316341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32464d84a837fd8f6b8288627424a1b99fa122fd2aa793bd118cc24b9afb6a8`  
		Last Modified: Thu, 05 Jun 2025 20:27:30 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:f66a2522f74d5d81688380fff66e787f32e0577ede9eedc4a070d8f036091fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344244827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235550725ff7dc299e89106f9494d9d815056a6609875c2c1db48222e2922f6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 02 Jun 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 02 Jun 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 02 Jun 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Tue, 03 Jun 2025 14:32:56 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Tue, 03 Jun 2025 14:32:57 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ee6650503f61f7673e0e24a6dd664f60276782494037ad8beebfdc40b05f7a`  
		Last Modified: Thu, 05 Jun 2025 20:05:21 GMT  
		Size: 92.7 MB (92726457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59517f64f93ef3235377e65403c21a43aa149e3627f878c0069b20d4472659dd`  
		Last Modified: Tue, 03 Jun 2025 19:06:17 GMT  
		Size: 124.5 MB (124514164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5fb018bc9a17ae92d58001917624bdeb8bde2a604421e9aa4deca2244f9860`  
		Last Modified: Thu, 05 Jun 2025 20:05:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b435d39a9dabacc3a5514e12dc259faff1e2bf7b0629b5a949ba0b25c7a22672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fde131e5fdeaec6f2158890de338d3973f49e3870fe270ef9f8ab99b492134`

```dockerfile
```

-	Layers:
	-	`sha256:bf9756b7ea390245d228b674e9cbdfa3490af50e103719f5a267624d794c14d1`  
		Last Modified: Thu, 05 Jun 2025 20:27:37 GMT  
		Size: 10.3 MB (10304372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0522ffae4e5b98184cb052573283829243728d25a4c9728204e3a9e839845e89`  
		Last Modified: Thu, 05 Jun 2025 20:27:37 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
