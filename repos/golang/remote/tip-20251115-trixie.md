## `golang:tip-20251115-trixie`

```console
$ docker pull golang@sha256:4e56ac83ecb262f8f8707d746b17361375cc3732c86c64dad7514798cb58d324
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20251115-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:9754d9763a9e7601a387721dd445766654c6b75f7f3001c974be8445232dad19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292922659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755a97715e4c04990f80ff56b1b08ccad53b4a6a45e8bfd13680f32e4e109ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 17 Nov 2025 23:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:22:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:22:20 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:22:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:22:20 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:22:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:22:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:caaccdf8fb49cd124dc4c23baaca3be5aad18c1263c8afe3356d15af000e612d`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 45.7 MB (45717135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1368971cf52e52bedcc9c34f098c9d72d70d67b7064ef11faefe431b570e27f9`  
		Last Modified: Tue, 04 Nov 2025 00:40:16 GMT  
		Size: 23.6 MB (23617115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5622b4d13fac6a61fac2dedf72d7cec257ecd1acee5ddbdff6f27c4b9ebc7331`  
		Last Modified: Tue, 04 Nov 2025 03:07:13 GMT  
		Size: 62.7 MB (62721595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69acd0f71be3f953a1a11fd397e536f9f251d93a4e6ee511a3f907865ee653`  
		Last Modified: Mon, 17 Nov 2025 23:23:19 GMT  
		Size: 72.8 MB (72753940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2c69f85dc047cff5b8e0c725d241fb21eed7123e04e156a844669a6e5e5d3`  
		Last Modified: Mon, 17 Nov 2025 23:23:14 GMT  
		Size: 88.1 MB (88112716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe4903054d605fc28399182dec28e10960002ea5f8ffedb791774a2b31efdb9`  
		Last Modified: Mon, 17 Nov 2025 23:23:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:dc3d47c153d937c46c2ac183171744d96ea2cd161c213466443cefd698851b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3ad2f728e506ff81e86ed20d8b418628437624732ce22703621b8ad73a4e84`

```dockerfile
```

-	Layers:
	-	`sha256:c3260f9db9239c40ff36a8d425b923d8251f31fd0f53d426c222d5184edf78e1`  
		Last Modified: Tue, 18 Nov 2025 00:23:24 GMT  
		Size: 10.6 MB (10580347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11018d0bee5ad64e3829901d3246eeb30cb4e71a7e7f8b83216a592c3679f883`  
		Last Modified: Tue, 18 Nov 2025 00:23:25 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:307c327c4683649fecd89f4a77df9024934315b53de6b59e759fe10c1d3e2c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327684532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a392791429cd6ed9f6513d805656307790cb81782d2c83e4ad9d989fea68e347`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 17 Nov 2025 23:28:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:29:38 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:29:38 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:29:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:29:38 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:29:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:29:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d671246164e1f42df8c3591ccbea2cf38af3f3d590719edfab37a99da881dce2`  
		Last Modified: Mon, 17 Nov 2025 23:30:26 GMT  
		Size: 98.3 MB (98254755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72859aa41c7126c75b0eaa6f62530c6ab6d97e63fe3d290a8c1d237f80407685`  
		Last Modified: Mon, 17 Nov 2025 23:30:36 GMT  
		Size: 87.2 MB (87177738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5225d9c77266020ba8f685b9e7c24cd390e8d2eb0778c56990172d05916b7a0`  
		Last Modified: Mon, 17 Nov 2025 23:30:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:bd0ce5a2ba47eb643b17ad62e1656e151a32897137fa1a93c9869da7bc88197a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d9cf1465d7fc64947dc04b040f86b1f4a13838dc625caae4e6a829dcddccc2`

```dockerfile
```

-	Layers:
	-	`sha256:d464ee237a460d27f818c29ffe7b074597fa0a25d8e385e9c1a0d1f7efdc6e01`  
		Last Modified: Tue, 18 Nov 2025 00:23:38 GMT  
		Size: 10.9 MB (10904915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61047d618f8fcbdd952e93be9c8a2879491262d0fac7154baf88b70376a02308`  
		Last Modified: Tue, 18 Nov 2025 00:23:39 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; 386

```console
$ docker pull golang@sha256:1229025ec53ec00625cc49daf52393946e6456663939f11806e5b1ed2f6751df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337831346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ecd7b7ad6bef3ba781fd2f3a390e7c5b805eec7796a06c23e05b925295e11`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 17 Nov 2025 23:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:23:10 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:23:10 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:23:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:23:10 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:23:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:23:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:933c2eb03a495d1bdbab772ff092366c6df6bb75cafd8749623e94908401abca`  
		Last Modified: Tue, 04 Nov 2025 00:13:58 GMT  
		Size: 50.8 MB (50801238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac49d94324079b69237b0b1612a8d78112618ce6800066877fb7d7a38ff9e74`  
		Last Modified: Tue, 04 Nov 2025 01:32:28 GMT  
		Size: 26.8 MB (26775967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1318169541c4f79fbdfc20cc98993bc7ba60d45d8f2235f647857ce150c6f7`  
		Last Modified: Tue, 04 Nov 2025 02:20:45 GMT  
		Size: 69.8 MB (69793982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7101a1d68c2d9e964ba733d4a09106a0aef25ab85c6da8c141ba70fdfa1b20`  
		Last Modified: Mon, 17 Nov 2025 23:23:59 GMT  
		Size: 100.6 MB (100555105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb363788838918ac7e550b93200cd675ca2501f3ca5b79cee14723fcfb2dfe5`  
		Last Modified: Mon, 17 Nov 2025 23:22:28 GMT  
		Size: 89.9 MB (89904896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fe5f5e5696afc1463cba2093d5d6ee4d54d47f36a5f625446586a5f02af636`  
		Last Modified: Mon, 17 Nov 2025 23:23:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:52511abb86fd23b6f63da5435ba97a45f71cfce3443143f0676422485c2bde23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db591b36207cd45aa6b5bb2fa3eba9e6379880b02004d2a5c4ed3e1bcd2a82be`

```dockerfile
```

-	Layers:
	-	`sha256:0fd328a7546dff213591f2e654895c72857b860dda17b4a95f23b387bb784858`  
		Last Modified: Tue, 18 Nov 2025 00:23:48 GMT  
		Size: 10.8 MB (10755724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a43c88d9b013eb6f4c26e9aff17ab89fcd5b247a8c41dbb745d5673c635aa9b`  
		Last Modified: Tue, 18 Nov 2025 00:23:49 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:c1edaff5d35366d9e7c82fe195c4f8d8e760311850e6052af33dc2c5258b6b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334595971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfcfc208f2314616786f0087016a9e90af311a9cbd1403fbbe8854afc4cb7a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 16:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 17 Nov 2025 23:46:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:46:01 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:46:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:46:01 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:46:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:46:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c598502b2d4d7d278f56bfb7b6960ccd64d116b7bc7b02516bad5cdad4a631`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 27.0 MB (26996633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbe8662034d4013b7fae91328f939dfb669ce78f36e4a91a9a0c68675f61828`  
		Last Modified: Tue, 04 Nov 2025 16:03:22 GMT  
		Size: 73.0 MB (73035332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bf1a7a31596fcf3c8fbba7ff2eb1b660f7e0a6b2bf397a661a0ba4967a80ad`  
		Last Modified: Mon, 17 Nov 2025 23:48:36 GMT  
		Size: 92.8 MB (92815616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c17fd7fd0e8bf95c13c3a94bedc5db23eb0e60440acf59ef05963d43e52ee79`  
		Last Modified: Mon, 17 Nov 2025 23:48:37 GMT  
		Size: 88.6 MB (88638105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38e147750a80771350283c7887ecbb2a94636415349ad0a8d4c2dae0e34a5bd`  
		Last Modified: Mon, 17 Nov 2025 23:48:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2b314f4ba22feda755846f3dedf00a24bbf182f19bce23bdf6f346c769a94e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b1a5f93fcec9188d70ab7fa9e0d77a6bcaa86e3fecadb0b0904f1077a388ff`

```dockerfile
```

-	Layers:
	-	`sha256:7c4360bc1a5f698c1c74aaa7edc9b6dda6c4b319d5db5e96364321c7ef9967f4`  
		Last Modified: Tue, 18 Nov 2025 00:24:01 GMT  
		Size: 10.8 MB (10780246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16acc58efb670e92501a59d2ae014ea227d2a27b671e7f5e3860430b88cc811e`  
		Last Modified: Tue, 18 Nov 2025 00:24:02 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:2dcc7dde88df5479f6648361700c229a28755dafb0cbb4c9836cd89d6ee6fb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.1 MB (360100182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6c636e39b9d40706aec9bedb0f15df8319edd71a3bc18a50055ef1233fb32`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Wed, 05 Nov 2025 12:03:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:36:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 00:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Nov 2025 00:22:22 GMT
ENV GOPATH=/go
# Tue, 18 Nov 2025 00:22:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 00:22:22 GMT
COPY /target/ / # buildkit
# Tue, 18 Nov 2025 00:23:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Nov 2025 00:23:47 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb0e1c49c4b6326e11479d7f89ce5a78336570bca91aa46a373571186f6ab4c`  
		Last Modified: Wed, 05 Nov 2025 12:04:45 GMT  
		Size: 25.0 MB (24953956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed84703a94ab124c54334c41ec37609f785f60feaff7dd12005c2d2dec188e6`  
		Last Modified: Thu, 06 Nov 2025 07:40:32 GMT  
		Size: 66.7 MB (66660260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5117301a45a9645452ed334ab328ee4d4f984f3fd793be3e5538b330d9db70f`  
		Last Modified: Tue, 18 Nov 2025 08:34:49 GMT  
		Size: 131.6 MB (131594683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37ec3a0230c2d0fb9a920af1a0e3505c5c46ba754e2ed64bb7c5b5268656905`  
		Last Modified: Tue, 18 Nov 2025 00:32:26 GMT  
		Size: 89.1 MB (89120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9498e50ee3bdc17b55733e1c45e1813309477c732d1a1c1ca37a3e682144fd`  
		Last Modified: Tue, 18 Nov 2025 00:32:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a18cfd4dd3e492bd1177ff782f4beb35903910da8d99adedda712cbe61870f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5281ed29beb8902edb23f4e0a21d24f9f825499e6629efa44d8c25747356779e`

```dockerfile
```

-	Layers:
	-	`sha256:d8046cd5ae14f5a7c16afdafabb51c91db47bafb12f19974e93384182e799e18`  
		Last Modified: Tue, 18 Nov 2025 03:27:52 GMT  
		Size: 10.9 MB (10854079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad238755e780f5ab35cdd6a24b14ff486b6f43ec1dccd6aa350d8acff8af0a9`  
		Last Modified: Tue, 18 Nov 2025 03:27:53 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251115-trixie` - linux; s390x

```console
$ docker pull golang@sha256:d33dcb689e7677eb418b9b4f4425b64857bf9999b7520c3a4db3c75b5d5afbcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.9 MB (310871799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8302162eb5a9326fa34d1b648a71f33451f9c48c5dc536027cd6037bf94d39`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:52:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 17 Nov 2025 23:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 17 Nov 2025 23:26:27 GMT
ENV GOTOOLCHAIN=local
# Mon, 17 Nov 2025 23:26:27 GMT
ENV GOPATH=/go
# Mon, 17 Nov 2025 23:26:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 17 Nov 2025 23:26:27 GMT
COPY /target/ / # buildkit
# Mon, 17 Nov 2025 23:26:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 17 Nov 2025 23:26:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205358f383faecf1c434c76ac887bd7a626ec58dd373ab479cce2de6c6d63849`  
		Last Modified: Tue, 04 Nov 2025 10:04:16 GMT  
		Size: 26.8 MB (26783618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e263d619c54c23185f97b8200ca156bd013604c1f55c66784ca7069ae48ff`  
		Last Modified: Tue, 04 Nov 2025 14:53:19 GMT  
		Size: 68.6 MB (68638436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6f9dd074bbc87474ed0d916d6b0462383f41a7e4cd59385eb488b43b543912`  
		Last Modified: Mon, 17 Nov 2025 23:27:17 GMT  
		Size: 75.9 MB (75919379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4515f8b1d9cf2143fbca8f466beb9046119009ff0c9973ec41a536bfa5dddca`  
		Last Modified: Mon, 17 Nov 2025 23:27:17 GMT  
		Size: 90.2 MB (90177909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29281560f849cd001a4a8dd824206df7b97544503aa19c41169460eaed51ff34`  
		Last Modified: Mon, 17 Nov 2025 23:27:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251115-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:efc6d73fa34c0a32a8560fb245e8fe209f1a475a69a0e67dad5736a7fcaa3319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a373cf4e503e23e7579e35ab649ebe3cc14f0847b71b3ad116387ef89c41ce`

```dockerfile
```

-	Layers:
	-	`sha256:f7f83b2d8bd72e4c4c9ac1c482f0b6e25c6305fe313e280a69ee9626264e26f6`  
		Last Modified: Tue, 18 Nov 2025 00:24:11 GMT  
		Size: 10.6 MB (10594860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ac0ba53665547faa8b2ace21ac79834e60f6797392d05e5ff8cead6b0f5f47`  
		Last Modified: Tue, 18 Nov 2025 00:24:12 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
