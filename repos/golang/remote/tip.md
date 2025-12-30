## `golang:tip`

```console
$ docker pull golang@sha256:612c8d0d8169e08b500a0edefbf3ca74f6ea196bcb922bfe88eb1b4e3c6684d0
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:85a96785e9f9884052abf21fe29dceccc7d0f4c5fb6298598148b429209ba8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339828683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba96e69925787a108c06dec354d32a2015613b53edc95a045964ead53e4d17`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Dec 2025 05:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:21:16 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:21:16 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:21:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:16 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf6916cd7b7ebfb12c4c89229cde50883aa41ab7b1012d4b34c2d815ea2daa9`  
		Last Modified: Wed, 24 Dec 2025 05:22:03 GMT  
		Size: 102.1 MB (102108834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8ab74e427643c28187f0d3b567e6fea07c0d44d52df85de53b9ccdd7a063e`  
		Last Modified: Wed, 24 Dec 2025 05:21:26 GMT  
		Size: 95.0 MB (95037660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c631df8c1fa4969e8d22d7fb418abe58e01993a4586e80b956e26a0587626e65`  
		Last Modified: Wed, 24 Dec 2025 05:21:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:329484d36dd6ac50d151fec25403dfc474292f99660149099612a9089fcd727c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2f1eff0c03dadff42c90c8338f80041f01bb8092d61b7329586797df3859db`

```dockerfile
```

-	Layers:
	-	`sha256:7c18f44279a44e1024e5ab0735d517133535c51cd6ca9123c30652812ff80418`  
		Last Modified: Wed, 24 Dec 2025 06:23:51 GMT  
		Size: 10.8 MB (10784508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f4a452772251feffbe4aa0beef6a3648bb1d6c9fca8547a0212143622043285`  
		Last Modified: Wed, 24 Dec 2025 06:23:51 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:1fc2671e3ec5d05a59701ae2cb22bfdf7baffd273081e811f831ffd6a86132c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.9 MB (295912027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb458513c44ff9de62da5b2b35883fff18e047b897b3f224bbc7111192582970`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Dec 2025 05:15:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:17:38 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:17:38 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:17:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:17:38 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:17:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:17:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693aebc67c5fe5e91be1db3da3bd28c72e6c8b000fe45e43f46c386babb33519`  
		Last Modified: Wed, 24 Dec 2025 05:18:18 GMT  
		Size: 72.8 MB (72754174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8916e480570823a95137488489c184e78cf3bafa0a643be0c57f52f82930a006`  
		Last Modified: Wed, 24 Dec 2025 05:18:05 GMT  
		Size: 91.1 MB (91105827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a083ba50e969120819fc948fd1d0af761ad64787135453be44efa470956690a`  
		Last Modified: Wed, 24 Dec 2025 05:18:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:4514d9825699e0bd74ea782dfbcde03d318185ef15bf2b3fcf41f1f35c851e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e010c0d9efd8034015434ace33c24ce96eabd5ab50ace3d8864c733cd368eb`

```dockerfile
```

-	Layers:
	-	`sha256:1a7779da3be7b6d8e53fbaa9771f3fea617319d11563d81aeda6fd1462ed174f`  
		Last Modified: Wed, 24 Dec 2025 06:24:00 GMT  
		Size: 10.6 MB (10580395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:214065d0fb001b8129f4cc0a8e020ef19902ee30e18a5f6c2c692140681c7704`  
		Last Modified: Wed, 24 Dec 2025 06:24:01 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:428c16282e1b7956bb7120951ff424946f9bd8629fe1517ce52eac7904d7ceb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330624303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43f1a24aceb470001831eef5c5592d9f4d32cfbb53f1d617a89fc6a8d4f3ac7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Dec 2025 05:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:21:35 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:21:35 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:21:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:21:35 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:21:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:21:37 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c1b32118dea358556db38f07c8cc55e9a1d276368b516adfb94c06c8017401`  
		Last Modified: Wed, 24 Dec 2025 05:22:18 GMT  
		Size: 98.3 MB (98254480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1a52724d12595cbdd937d1a6f8220032f161596f409cbf2928a4904bc545b`  
		Last Modified: Wed, 24 Dec 2025 05:22:14 GMT  
		Size: 90.1 MB (90113486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b97978b3773ce7e204cf48b0b91265cf7dddaee018d4e079a2b3428630edf50`  
		Last Modified: Wed, 24 Dec 2025 05:22:12 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:9155835e3308b010966bd7ee56713b099eb4888bbcd7e486e4d4a345b1f8a0ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353f49f416c94d2bcb83040f6f5dc69e3d65b0fd2bdcc38473bf2c3e60385409`

```dockerfile
```

-	Layers:
	-	`sha256:81878475a819786b5b7191fcd3b45fd90eebd3e3cac51a3b7cb6229824769a0b`  
		Last Modified: Wed, 24 Dec 2025 06:24:10 GMT  
		Size: 10.9 MB (10904963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20dc5e01004d77ab579559bc69cbb1b1dd96515678bd584f867a29320be4be6`  
		Last Modified: Wed, 24 Dec 2025 06:24:10 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:bc8740b0a23438fababc25ef7b02eddd568039eb44d06eafca9989fd93419fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340867058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebed657f9fe3d6d305e93ba294fc1f076307d4b991d41f568fdad334cb3b617`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:19:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:20:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 30 Dec 2025 02:20:54 GMT
ENV GOPATH=/go
# Tue, 30 Dec 2025 02:20:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:20:54 GMT
COPY /target/ / # buildkit
# Tue, 30 Dec 2025 02:20:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 30 Dec 2025 02:20:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ade73e32bbbd03836491e06521d1ebd5a0fba60e525afdeb3262e68c8b12d8`  
		Last Modified: Tue, 30 Dec 2025 02:21:36 GMT  
		Size: 100.6 MB (100555344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b6f0074455116012c1ba771d20edb2ec10d2462257d60366f8ccb9b9224a99`  
		Last Modified: Mon, 29 Dec 2025 22:17:35 GMT  
		Size: 92.9 MB (92938705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a65206a294cfa58d808be4d6044b7204f516d26da0fec139e2c57b03be9a1`  
		Last Modified: Tue, 30 Dec 2025 02:21:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:3bc67aadef44dc3ad0700152f0bfd453c7993fac049bac083f047862baecbd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a90c97ed07c1ad0155a5249054172c4e109379c387a5897912febee0bb27ab5`

```dockerfile
```

-	Layers:
	-	`sha256:1c749b3b4963e1aea78097fb43c83853339e3f9046ac18c21de8ae2a2521aaae`  
		Last Modified: Tue, 30 Dec 2025 03:25:46 GMT  
		Size: 10.8 MB (10755772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cb1784d9e4461ec2c758c3a218ee7e821afd14cab59868c8cb3cd07edd94a60`  
		Last Modified: Tue, 30 Dec 2025 03:25:47 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:a9c28777fab2c497c3056b8349ee96e1f5b8615cf728c1622096230d79bc2c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337598525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09889bb1707f24978da604f1af9bf8e2db9d33b4deadee75e3b71213f70b68d0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 06:20:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:34:00 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:34:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:34:00 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:34:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:34:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62094cf6808b342239ceac9c58c9096b769bf275793baaa6699740b93ef88f7b`  
		Last Modified: Tue, 09 Dec 2025 06:22:27 GMT  
		Size: 92.8 MB (92815776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5de3a0302474d051f06a0dba49ec72e6a84fba75a10ec5c8dcfe3ca9da396d`  
		Last Modified: Wed, 24 Dec 2025 05:35:28 GMT  
		Size: 91.7 MB (91655252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30c94c99f27d1cfbe02effe868908c59561813d2dc6f8a09e09c5a01d54fda1`  
		Last Modified: Wed, 24 Dec 2025 05:35:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:30c390c6493e88367f86bd759e35aa3ae4d5918a144ddf74cc72c9a8ee22ce2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74a76dd3b0ad62f293886311c491cc047f8eb64982afa74678acef126ed4c1`

```dockerfile
```

-	Layers:
	-	`sha256:ba7907559710dff4f02811badd97b83e7275d846c7f6a380f0ae9cf70bcb9acd`  
		Last Modified: Wed, 24 Dec 2025 06:24:29 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772d904105f26427c92b9e7c8f8bb916854db9263aa0324cbfdc908c689e19c0`  
		Last Modified: Wed, 24 Dec 2025 06:24:30 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; riscv64

```console
$ docker pull golang@sha256:7952b6372477c6d07bd3099ffefb74cd51eb30854438c9240fd9b6e6494bb17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363279010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce951910c1f9f828dfdb57255fb0da99fae679dafbc70efc653cebaa1d591c30`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 07:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 06:56:42 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 06:56:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 06:56:42 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 06:56:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 06:56:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4af291d8cbdff6d28ddd144cb820c9d50e09d2eefe7cf2deb9f3384fddd0193`  
		Last Modified: Mon, 15 Dec 2025 07:10:40 GMT  
		Size: 131.6 MB (131594746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efbeb47d67a4f0f513126184055d20de04c0261cfdbd8b06feaf3a27c3f0eb2`  
		Last Modified: Wed, 24 Dec 2025 07:04:00 GMT  
		Size: 92.3 MB (92298638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be72a4e09c8ffe6f8ce6556e995fa8ab56ec582d1f2b14a2864dc979ca88ec42`  
		Last Modified: Wed, 24 Dec 2025 07:03:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:6d38cc12d2f36c041c99a1f950b63ef191ed2c3b33e6cec769d7a65e580055b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99edd8d350026be9177f1067a1ec6e85b7f736022a00d76b647e8f9ccdf7e06`

```dockerfile
```

-	Layers:
	-	`sha256:eebc122be4fa3e0f80e64faedb8c04a7a7a0c3147caeba5aa00a9c900dcd2a29`  
		Last Modified: Wed, 24 Dec 2025 09:24:03 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a56a7dc2f384f11c5c114e514fd0ea65638e1bfaf2742bb04a7519f51d78f79`  
		Last Modified: Wed, 24 Dec 2025 09:24:03 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:57dc55808c4a5c88127ae2058ba38176e0f76adadb8247fd115cdfd252bf2be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314875221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350bf60ae1561162d97c85cb79e1014947b9d88383a93b46908ff65d73ab8d4e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Dec 2025 05:16:18 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Dec 2025 05:16:18 GMT
ENV GOPATH=/go
# Wed, 24 Dec 2025 05:16:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Dec 2025 05:16:18 GMT
COPY /target/ / # buildkit
# Wed, 24 Dec 2025 05:16:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Dec 2025 05:16:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2be274f95003449a8278cbc7ab315c7bcb675710ce099ea39eaa8742edd0f0`  
		Last Modified: Tue, 09 Dec 2025 03:00:19 GMT  
		Size: 75.9 MB (75919454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eae26383a5ec3ad19d41ec233e74f5aea1ebfab7013779b5b7f518483b785a`  
		Last Modified: Wed, 24 Dec 2025 05:17:11 GMT  
		Size: 94.2 MB (94198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6034d6bb260ee37a79a943ccdd639854251c8c9114a11d483872c70a7d15b5`  
		Last Modified: Wed, 24 Dec 2025 05:17:05 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b2ead00a4d7fea96d80fe37d9edea44a059725adf2d56df88e2332a740438f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d56d16a50f4f02c6c95f502c8153a6a1bc8c31db58eff1a2f7948ac96c90e41`

```dockerfile
```

-	Layers:
	-	`sha256:30b420beac0fa4c147d2262578ea58fbaa97d4b72319ab6b302fb708e0340ee2`  
		Last Modified: Wed, 24 Dec 2025 06:24:38 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12f08cbc7dc6840b4aaa21f02cdbe1d789de6a738f157bf461e1bfbf3c302c57`  
		Last Modified: Wed, 24 Dec 2025 06:24:40 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
