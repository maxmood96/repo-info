## `golang:tip-20251102-trixie`

```console
$ docker pull golang@sha256:fe366a4b441cde53e2a64074a035a9845a99a6e870147ce0b998ed6dc0bf33eb
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

### `golang:tip-20251102-trixie` - linux; amd64

```console
$ docker pull golang@sha256:380df26485f6ba4b4ea3726857edbcb564a56b3ff6ae54145d71e032235700c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336393114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3dbb4d2ef562f5e93ab497e5e3e6093ba0e3d58cb1c07490c7e61563c21631`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:26:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 14:28:36 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 14:28:36 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 14:28:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 14:28:36 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 14:28:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 14:28:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6bd1abe523fe471f941612fe664fb2fa8924719acd724ee5502ab788756429`  
		Last Modified: Tue, 04 Nov 2025 14:29:21 GMT  
		Size: 102.1 MB (102088409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cdc461d8e5b6378706696b9d7cb2bee286c3be63889d089612a96810cc10`  
		Last Modified: Mon, 03 Nov 2025 18:07:51 GMT  
		Size: 91.6 MB (91626668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10a9db956886309f304eb9292f240186021d263771cd46e5347e9148a920e45`  
		Last Modified: Tue, 04 Nov 2025 14:29:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7c92f29f3ed76a0c2ffe93568f32cbd00a85e76596247139afb611ad0d0d4349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6525b06cc41281392bbe4b2deca4dbabf18e3f6710eeca55dc56b95e117f8783`

```dockerfile
```

-	Layers:
	-	`sha256:2803b861080a344f9a5ca71c6641d45a3893ab73485a40fabe5055807c3901fb`  
		Last Modified: Tue, 04 Nov 2025 15:23:17 GMT  
		Size: 10.8 MB (10784460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00979abd64f6c8563ff7ba540c6900a484593f84ba187060b9d236d55b251b5d`  
		Last Modified: Tue, 04 Nov 2025 15:23:17 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:3d2e8cd999be040db54c9ab20debacd2f8c831f6a3a5d1ea1d613be86d0dc918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292596471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52505042af7a9b7f02a838187c431c31b64ba94b4295c698aaf4284a08f8127`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:32:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:35:17 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 04:35:17 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 04:35:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:35:17 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 04:35:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 04:35:19 GMT
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
	-	`sha256:bebb9f05f53ddd1129df46d659282e6cb91acf2d6d07eb78f8acca508d5d0de1`  
		Last Modified: Tue, 04 Nov 2025 04:35:54 GMT  
		Size: 72.7 MB (72733789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc3193360041d5ec3fd6b5f23bff516805dac965b3e6d2a23e404f02fefd2e`  
		Last Modified: Mon, 03 Nov 2025 18:10:00 GMT  
		Size: 87.8 MB (87806679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb2258a448892f25d9612b0a450f71d727d33fbeb93197a805921999d4d76b`  
		Last Modified: Tue, 04 Nov 2025 04:35:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:df7ab5bf87211cc7540d2142f53a153300a6c951004fb8e25e663b733bf35c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2976cff35222b6e64fc04155d0deda177b951e00d551b748e96ea2f94bfa0067`

```dockerfile
```

-	Layers:
	-	`sha256:896752ae7e83550769611a4b373a4692ae44fcf1c3ca6125dbabd64ba6804544`  
		Last Modified: Tue, 04 Nov 2025 12:24:27 GMT  
		Size: 10.6 MB (10580347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc4a89760690377fc82bc279435753bae7b18398bbc114f0bfcaf22a1a00d84d`  
		Last Modified: Tue, 04 Nov 2025 12:24:28 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:8a172387c32addea6d53b9e7e9e6562d9b3ec89da2d8453b7db7c8bde939dc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327364607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbb6e1d7303f5913f3685f1160ade19616d5b2f2c6e6fe46a8a37e74522f657`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:17:26 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 04:17:26 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 04:17:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:17:26 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 04:17:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 04:17:29 GMT
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
	-	`sha256:f9cb33df82d5e58d11ca11c5c6df07823a8d46db849f4b71b3bcb5ed4c4e6f7b`  
		Last Modified: Tue, 04 Nov 2025 04:18:15 GMT  
		Size: 98.2 MB (98233997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a31d309655c21bc621f07e8c42b1089ab055b4f9c298c53b0ddf3b945ebd2f`  
		Last Modified: Mon, 03 Nov 2025 18:07:42 GMT  
		Size: 86.9 MB (86878571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c913cc89c7cb9431b199b5dbd50768b270b69197f94675902aef8d0f270640d`  
		Last Modified: Tue, 04 Nov 2025 04:18:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:49c42f1025bcd750bdff58931808c932e82509b041592bdf26d48469ac93a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0341d32b74c119fc60f037e16b46a7ba3db5da3323fa1deba7bf6f6ce51ebc`

```dockerfile
```

-	Layers:
	-	`sha256:8917e6c3232fcd33838f835b06a4b8efdfd9d062d60150b3100e5cbfa7230036`  
		Last Modified: Tue, 04 Nov 2025 12:24:35 GMT  
		Size: 10.9 MB (10904915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6e062b9d9bba5ffb555122b50bd7052de91d0910ab6589b24deaa28f1c4b4c`  
		Last Modified: Tue, 04 Nov 2025 12:24:35 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-trixie` - linux; 386

```console
$ docker pull golang@sha256:fde522832e887183a55585b2bb06a4817e84ee47b6f70b57684985a143b2b29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337517284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097a616dc0b6687dd5dd332938d27b78f2c1313d46f229d014ed47ad47866bd0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:16:09 GMT
ENV GOTOOLCHAIN=local
# Tue, 04 Nov 2025 04:16:09 GMT
ENV GOPATH=/go
# Tue, 04 Nov 2025 04:16:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:16:09 GMT
COPY /target/ / # buildkit
# Tue, 04 Nov 2025 04:16:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 04 Nov 2025 04:16:12 GMT
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
	-	`sha256:ef7e11b5c4860757bc5a0fa86b2a3e411042d9bcd618775f3c7b05fafffd3b6f`  
		Last Modified: Tue, 04 Nov 2025 04:16:52 GMT  
		Size: 100.5 MB (100532912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db89236eeebef76fdc6574b93130c4a0c99f66c249e46e945ed95e5d140c9856`  
		Last Modified: Mon, 03 Nov 2025 18:08:37 GMT  
		Size: 89.6 MB (89613027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083afc821ada5080f3c904df5f548b65173efc529783c731bdb5df52b6a71509`  
		Last Modified: Tue, 04 Nov 2025 04:16:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:870c091edf3ab1961c6a346277a2e099abb5ebc303ffab4160572a658dffe2e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1b70269ec34b091b8f2f4696b09cf3599eab55e0959945c2ffcad612e998f9`

```dockerfile
```

-	Layers:
	-	`sha256:c1b975d3ff287ec4cdc67446481b91eb45c41e72dd8165272ede39bc2f154a04`  
		Last Modified: Tue, 04 Nov 2025 09:24:47 GMT  
		Size: 10.8 MB (10755724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984b9c0d8e36cf8be86c007857b8b330e1dedabbae96f71aaec0614ce6b2f16c`  
		Last Modified: Tue, 04 Nov 2025 09:24:48 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:c1c0056697c4c57e06bab2514dd9459d6d5c46bfe754297fc35fc5c965002c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334222463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282383e8cf167b536caf3567e123d571562e1c9d8f6ac2d99e62b91030534e67`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 03 Nov 2025 18:08:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:40 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:40 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 18:08:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 18:08:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b8892ea040f8ffdb59a5551839a9c9b444ca569d6e9b5ac4b2e1cf5e439855`  
		Last Modified: Mon, 03 Nov 2025 18:09:46 GMT  
		Size: 92.8 MB (92795074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11f1fd4cd7eff0746fa6b81e430f63f5332dd96bd03a2e634ca5fc29dcb745`  
		Last Modified: Mon, 03 Nov 2025 18:09:48 GMT  
		Size: 88.3 MB (88291863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27329c12bddd5ee443948da06e76536b81b7489ceac8b5124e58e2fce6ec8f1`  
		Last Modified: Mon, 03 Nov 2025 18:09:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4224bfbf80acb6fedbcf5eee25f4de0ac06b612bc81d3f040ba6ddb80416ec43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dc6070f3aec5072d5bda16960836c6714a6d1464ffacd2732693ab963bf085`

```dockerfile
```

-	Layers:
	-	`sha256:5bcb6cc05192aa5ff97ec3636512c1098f0dc92cde55a24fabfd9e26988371f2`  
		Last Modified: Mon, 03 Nov 2025 21:24:09 GMT  
		Size: 10.8 MB (10780246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34e68720e523b97fd5a7b7b50631296d615cc64affd7f772795ca273749747ec`  
		Last Modified: Mon, 03 Nov 2025 21:24:10 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:7304ec6d155dd4ea14e2c1812d1143978de41627e1ee7fbc9d4def6ca617eafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359760662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ea34ed60de26c82234007057ffafb9c0e266cb4d376afb70a36062575329813`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Oct 2025 12:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 19:28:57 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 19:28:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 19:28:57 GMT
COPY /target/ / # buildkit
# Mon, 03 Nov 2025 19:29:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Nov 2025 19:29:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c640441904d97046ee4a137483e3b6745e0a18782c3b688fede8e9ddf18261f`  
		Last Modified: Wed, 22 Oct 2025 18:09:29 GMT  
		Size: 25.0 MB (24953874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cb6fec5cd2588ba9a09a9491547b6e7005f3640a81c530cc1f2e651257c901`  
		Last Modified: Fri, 24 Oct 2025 21:34:03 GMT  
		Size: 66.7 MB (66662364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3fb0e7079a4b7a9ec6d9a3b797f899acb3726d9808ef2e02cbb7d243e4a418`  
		Last Modified: Sun, 26 Oct 2025 14:28:28 GMT  
		Size: 131.6 MB (131577542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568766c8d70cce8f34aaf3713ad1c1267acad6ccddf02bbbe3d428a4c87f11f0`  
		Last Modified: Mon, 03 Nov 2025 19:36:15 GMT  
		Size: 88.8 MB (88796418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c1ef3333370fb80ffd289766a261d792c670658025300db42c16c438fd98a3`  
		Last Modified: Mon, 03 Nov 2025 19:36:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:60c608cf180527206cf189623bd1e78e2487b65486a74011c542cfb110a5ad33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74d441766ccb9f84acd2b02bec069ae234a1f6c517314df2b29a28689f45932`

```dockerfile
```

-	Layers:
	-	`sha256:4a5015fa9192b8178742ef7d25fc8f4c990f501f13fcaf9c56a4b9be922d5267`  
		Last Modified: Mon, 03 Nov 2025 21:24:19 GMT  
		Size: 10.9 MB (10854079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec745d5be2ea4935f0de8ccfdabd6973f130340278c19102678aa1760c5a112`  
		Last Modified: Mon, 03 Nov 2025 21:24:19 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251102-trixie` - linux; s390x

```console
$ docker pull golang@sha256:f80e9f8700de6424f9a9faff204ff3a426efa5ef1cb387c2ca4ace4f96c86eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.5 MB (310511127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e113536e1178857ec37fef4b2aa50102ed6b073442e9876f7cbc9bc88a74f110`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:52:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 20:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Nov 2025 18:07:02 GMT
ENV GOPATH=/go
# Mon, 03 Nov 2025 18:07:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Nov 2025 18:07:02 GMT
COPY /target/ / # buildkit
# Wed, 05 Nov 2025 01:58:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 05 Nov 2025 01:58:33 GMT
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
	-	`sha256:8212989b5ce73204da0c743d787a8c42e4101ff5ee0c2d0eedd357f04a43945c`  
		Last Modified: Tue, 04 Nov 2025 20:12:57 GMT  
		Size: 75.9 MB (75900226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801db4c6115aae59bd4317ca926bef2957dbc3991dbc119cde22a6ba6c9c43c7`  
		Last Modified: Mon, 03 Nov 2025 18:08:18 GMT  
		Size: 89.8 MB (89836390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4739abcbfcd3fe2687fbb518032ffe2dcb09e440447b8032611c0d763bab51e`  
		Last Modified: Wed, 05 Nov 2025 01:59:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251102-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:454e03bedeb059c2ca19518f5c5f41aefe6471ec01e7d9244d6864249d3cf333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977f122254752a7afe436268b4e77e680c8f933229bee15aa0f9c4d4464fdfc`

```dockerfile
```

-	Layers:
	-	`sha256:1572be10140130a2a4fc401521f2b78690b183892724b5f9bb61170ae96f623c`  
		Last Modified: Wed, 05 Nov 2025 03:23:50 GMT  
		Size: 10.6 MB (10594860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ad1a55edafe202049160d2bf1c77228cbecd8c0a061b547005e59fb3eed47b`  
		Last Modified: Wed, 05 Nov 2025 03:23:51 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
