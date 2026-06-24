## `golang:tip-20260619-bookworm`

```console
$ docker pull golang@sha256:1201bab41fab1594e857dd6653a63e3e5842eb1372a5f978de87379d86fcba74
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

### `golang:tip-20260619-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:963494d596cd4da782f03294c6169a6dceb9499310f2ac016002deb9b01627d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.0 MB (331991011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cd410b48ca32e62c6d6269b3d7c20437bacffdd7201cc1cd3f012e9b644fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:18:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:20:01 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 04:20:01 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 04:20:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:20:01 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 04:20:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 04:20:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fd7bf6f6036613e20f62549df75ed694b99118002358bea5a81baf3929d1ff`  
		Last Modified: Wed, 24 Jun 2026 01:41:33 GMT  
		Size: 24.0 MB (24044046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791c68bc2063683c3d15907b8ed1b777cf14ca153c6f8e5b12db0868dfa7e38a`  
		Last Modified: Wed, 24 Jun 2026 02:28:33 GMT  
		Size: 64.4 MB (64404017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab24b4f4704eb64da61fae997e97a7a12f5ba708cf842b779175dbf802af46ff`  
		Last Modified: Wed, 24 Jun 2026 04:20:31 GMT  
		Size: 92.5 MB (92481192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ced9bfc2a0ce47376a0e89056fba2dbdc199ef992671e729f2b29cd85c5af1`  
		Last Modified: Mon, 22 Jun 2026 22:43:09 GMT  
		Size: 102.6 MB (102559388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a55bac8228d7d3af576c530a7d2ef1f5a09aa323543af847d001f4bcd943920`  
		Last Modified: Wed, 24 Jun 2026 04:20:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:7b9d896013e614ed9e8426f71dcec6a56deab6c723f595800ef24eaa1836b565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bba4a15b16b0b1d235614a7f2d53e1a2093f6227aef196322988c31c75439f`

```dockerfile
```

-	Layers:
	-	`sha256:4e43065e9299503216ff72da0d4bd15d3ce729c07c88bcd44a4d9c77d8a390ee`  
		Last Modified: Wed, 24 Jun 2026 04:20:29 GMT  
		Size: 10.5 MB (10497073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0cef1f0dee5257a5fa1ec041d381de04b30d645f7a1b67447f09d38c0ef89e`  
		Last Modified: Wed, 24 Jun 2026 04:20:28 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:9838301f48f3ccb19fcd1765e47af2145cf6b3bc3efeefa7e8d1f994a7dc3bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290435247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83904ea412d67735f0f564198650b09e9cd39021befcf6943311a270db214f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:54:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:20:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 05:20:53 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 05:20:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 05:20:53 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 05:20:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 05:20:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3622debffba3838b917703fb6dd9c161a4d93d9fd97c61d3e8400a2245f93c67`  
		Last Modified: Wed, 24 Jun 2026 00:27:30 GMT  
		Size: 44.2 MB (44208145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0df8de55f365d832099cabf27409104999d59b26292d91202ca6e160c4b513`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 21.9 MB (21949935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16c85bf5ff1b42ae66f83fdb64a6cd05a854ea2289dfe1b0ae9e4ee6a806d0a`  
		Last Modified: Wed, 24 Jun 2026 03:54:41 GMT  
		Size: 59.7 MB (59661949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb621f3b9a14d76acf9adf063e20791918e4f8b99c664bf7bb4216e5de38849a`  
		Last Modified: Wed, 24 Jun 2026 05:21:21 GMT  
		Size: 66.3 MB (66338900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346f6c0ac1bf1a1f35e41966874d41949d2c8d30b471f4a54f05d28249cc12bc`  
		Last Modified: Mon, 22 Jun 2026 22:45:14 GMT  
		Size: 98.3 MB (98276162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ee86394ccc05fc269e5e61d9e7c8c276053f3d15230008feef4fa115779744`  
		Last Modified: Wed, 24 Jun 2026 05:21:18 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:028bfd0b770dffac84dfc9f7cbca80d8813f78deeab9309688d7f9fac3693e12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6840ff58e73c8aac6465d4001c9a907dfdb054ff667141b306275643a8449d`

```dockerfile
```

-	Layers:
	-	`sha256:3fe948b20a3bf9f3e87dad79a6fab34fc0a8d8511847fdbfa107712de3fb52f5`  
		Last Modified: Wed, 24 Jun 2026 05:21:19 GMT  
		Size: 10.3 MB (10303769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a178f22b4389c77119fdeb2b1920dfc33ead727d8febbb7c10148b938893606f`  
		Last Modified: Wed, 24 Jun 2026 05:21:18 GMT  
		Size: 28.5 KB (28497 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:968b0094549c96614d8b381324631c4152cbc3b9e867e796aa92215871596439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.0 MB (320004372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edca1fd318df65ae05e24984008f1f70b8845e6b5a36f35b2bab0dc991630cf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:35:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:19:53 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 04:19:53 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 04:19:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:19:53 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 04:19:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 04:19:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ebca214f1a4b66acfdb0bd20aa3ee139d1747885ef4b0f3d07aa2a68459230`  
		Last Modified: Wed, 24 Jun 2026 01:44:48 GMT  
		Size: 23.6 MB (23613316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bb0e918720911be6cb7a1a5ba9ad0e1a308fcbf24961a23aba0cd220df6cf`  
		Last Modified: Wed, 24 Jun 2026 02:35:28 GMT  
		Size: 64.5 MB (64487706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee621f24a5ab1b28fd4d139fe77bb3061ba1b54b470211a4a037975a53deb0f7`  
		Last Modified: Wed, 24 Jun 2026 04:20:22 GMT  
		Size: 86.6 MB (86554547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a4f06fe9b49ab2b0e448e3bb545bf0083fe0a192a188b8354bf30a5042489`  
		Last Modified: Mon, 22 Jun 2026 22:43:15 GMT  
		Size: 97.0 MB (96959444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef24e3c1fc8a1bff3e3119c143fbe50c2435dd3b39c62356438ba75ecf910cda`  
		Last Modified: Wed, 24 Jun 2026 04:20:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e919bbcafe3bdd36289f11ee88a4f242da84a6ac1bfab20de142f06605129dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b75f0b43851233f7ad0fd879329037b05cbfa58390a5bc44f600817476dd054`

```dockerfile
```

-	Layers:
	-	`sha256:673749de1deedf8f694a6f9525c9f9d382b4fb749e7b23527088e4a2ace84a1d`  
		Last Modified: Wed, 24 Jun 2026 04:20:20 GMT  
		Size: 10.5 MB (10524897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9df5b713efca5504f6139f13c2c76adeb256b25a82e1a95f9c9c2ab8a5e98`  
		Last Modified: Wed, 24 Jun 2026 04:20:19 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; 386

```console
$ docker pull golang@sha256:c9f02466d4e31ff5043013b21dc34f71db96743af45552024c809d4fa671752d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330858441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120f1a91453b22aa6a312cd77b636c58baf74c21dcff8826a690592a8a40a526`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:34:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:14:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:16:51 GMT
ENV GOTOOLCHAIN=local
# Wed, 24 Jun 2026 04:16:51 GMT
ENV GOPATH=/go
# Wed, 24 Jun 2026 04:16:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:16:51 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 04:16:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 04:16:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96cbacad9c1883b9ae87f68a0550ac0bd7e0b7ba2b15b142a793b89b5a5f36ad`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 49.5 MB (49491378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b45c9ce5ae5ea6ab37787312be8b0a9732642c1221f97d5689baacac874b4cd`  
		Last Modified: Wed, 24 Jun 2026 01:43:48 GMT  
		Size: 24.9 MB (24879740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db0110899c29fd647e62f912bfb740fc8af5310cdc227454d8f086f16cba33e`  
		Last Modified: Wed, 24 Jun 2026 02:35:05 GMT  
		Size: 66.2 MB (66244204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2bcc22a1fe3502692515263d0cca8ef5dfb9a681ffa1f61de16ccf9e784d9f`  
		Last Modified: Wed, 24 Jun 2026 04:17:19 GMT  
		Size: 89.9 MB (89903966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3675e2fd1600788af1a6ae5db185dc20a1f52bf11f13c9afd16f6795c307c09a`  
		Last Modified: Mon, 22 Jun 2026 22:41:13 GMT  
		Size: 100.3 MB (100338995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad8f1bea57b7ba7c89c7ddcaca581262c0f9729c36fd240c5a01781edf31ef2`  
		Last Modified: Wed, 24 Jun 2026 04:17:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6d4c11aa4d1c68c803285bf84859364bfc3389fe5bd750e6b90d83cba5b48f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7feb52842a32cad04b37eac2d0f0b11b4ce38e81eaf8baf497f2536477976be`

```dockerfile
```

-	Layers:
	-	`sha256:2f56af7224b93b815daaa6589266b125df032a61d6a8714a083c326da338028a`  
		Last Modified: Wed, 24 Jun 2026 04:17:16 GMT  
		Size: 10.5 MB (10476653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:316a1097d3c477b61fb4bc26b998c729ef9fa97300fed6a501f406e0f81ad263`  
		Last Modified: Wed, 24 Jun 2026 04:17:16 GMT  
		Size: 28.4 KB (28357 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ea58a99235fd33176bcdadcb74dfcfbdef0d786b567c81e14296af522daab202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301746966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fbad091c8e6e0413fc2933e298f0315e728f4e19e8ba91aa7a0a4c5f84a978`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 17:08:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:00:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jun 2026 01:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 23:02:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 23:02:50 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 23:02:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 23:02:50 GMT
COPY /target/ / # buildkit
# Mon, 22 Jun 2026 23:03:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 22 Jun 2026 23:03:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c4a18bb29be3659c76b4d9b55eb7f69e2b6fcb341523ef1670ac059503a592b9`  
		Last Modified: Wed, 10 Jun 2026 23:39:38 GMT  
		Size: 48.8 MB (48792711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d391bb145fa329ccce2ad9a5e686a519ff55f48ee4a211ba2c146ad64db56d80`  
		Last Modified: Thu, 11 Jun 2026 17:09:36 GMT  
		Size: 23.6 MB (23624039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270c086020bbce3335fe9eece6ed9bd8f5bc1e45eed6579e81e64181addffb83`  
		Last Modified: Fri, 12 Jun 2026 01:02:23 GMT  
		Size: 63.3 MB (63315954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914bf280b1770cc8113eb19527c59fbb1740e0ce824cec4f0fd9e76670a4b8f6`  
		Last Modified: Fri, 12 Jun 2026 01:33:02 GMT  
		Size: 70.1 MB (70083997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae066d545f3a63cd46644c3d9678ba433b4c9aa20eb87d43ba7557e769fae2c`  
		Last Modified: Mon, 22 Jun 2026 23:05:12 GMT  
		Size: 95.9 MB (95930107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de9a358cc10d54f5f7fd269d1f737210b0b0d2587fcda60b5d39bf02fdfe741`  
		Last Modified: Mon, 22 Jun 2026 23:05:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4c8d329c9aecc1f0f4daeaa5e81b5a513414893c7075dfa1538ead1facb054cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78633b8b0cbed93e7eca133416f243981a147bd8f78f2a5a563c59457864bb5`

```dockerfile
```

-	Layers:
	-	`sha256:c66160855df8e01b53cae55c62320f8e9979a04e3ef09839890eb0e8eb5a7425`  
		Last Modified: Mon, 22 Jun 2026 23:05:02 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:3a97314a7ecc1169d4a6c4e25036a19e8ebbbf48eec1366c2ec9ee933a5c4125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.3 MB (337328555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23bc6f5836f3e73321532a3817633ffe99f8afa9e94abcc7c801c15bb89686d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 03:25:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 09:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 11:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:41:08 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:41:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:41:08 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 15:33:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 15:33:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a217268ac6656bd05839d5770fe7b3c0c976d29750b0c5635d099e473a789a10`  
		Last Modified: Wed, 24 Jun 2026 03:25:44 GMT  
		Size: 25.7 MB (25687048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6542f967f29885e49bf508e83dceee1eda4fdb044dcd68c1237588f15b795e2b`  
		Last Modified: Wed, 24 Jun 2026 09:10:08 GMT  
		Size: 69.9 MB (69853519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9034cb40d1ddee03957e235882d85c3935748284d5ce7d9e3b1fb946a360d593`  
		Last Modified: Wed, 24 Jun 2026 11:45:03 GMT  
		Size: 90.5 MB (90495696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ec7882ea306fbaa9d198836e0980a8d1968fa6de95f144db148dc1345d3f57`  
		Last Modified: Mon, 22 Jun 2026 22:42:20 GMT  
		Size: 98.9 MB (98945286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9a282a3d52dab70a089b0aeadf1676f350178b9322acc4f9968b383407f82e`  
		Last Modified: Wed, 24 Jun 2026 15:34:28 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:67ae69693e77342e2f8ee3b014893298b8606aea41d33334b26716757ff247c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec253caf75bc794cf01f965d603b905436036b6a6d317a03047c724caaa1ecfd`

```dockerfile
```

-	Layers:
	-	`sha256:dcbb3f76fc5efe85938558d8e3dda034d3f83acb2246788382c70faa3bab51af`  
		Last Modified: Wed, 24 Jun 2026 15:34:29 GMT  
		Size: 10.5 MB (10469558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50bbf842a8fc18d3794e7f608fcb8662e5a046b3fc54481c9535e662a9d984c`  
		Last Modified: Wed, 24 Jun 2026 15:34:28 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260619-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:9e1aa39ce64947182a43624ee4b72372919e8635bd3ce057e9648bf91ce37a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304796867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb89e7a2a43bc9819440cb53a097a3a709b57a2d57be94e9dada02de7dc9ef8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 04:29:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 05:19:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOTOOLCHAIN=local
# Mon, 22 Jun 2026 22:44:37 GMT
ENV GOPATH=/go
# Mon, 22 Jun 2026 22:44:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:44:37 GMT
COPY /target/ / # buildkit
# Wed, 24 Jun 2026 09:43:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 24 Jun 2026 09:43:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075239c7f31ef6bc9923503289fbabd4a216a0cc1314ab546cdb22b3aa178273`  
		Last Modified: Wed, 24 Jun 2026 02:46:07 GMT  
		Size: 24.0 MB (24038997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98bfd0e5e3c41d5610549c351f2a214a1057c70f21ae763c153398d8481275e`  
		Last Modified: Wed, 24 Jun 2026 04:29:51 GMT  
		Size: 63.5 MB (63498267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d1414b3e953738f356156292a7fa01dd82d03c5e49567e8b4a25ab7606d526`  
		Last Modified: Wed, 24 Jun 2026 05:19:58 GMT  
		Size: 69.1 MB (69087957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf953c950bf774a1558a2610c27217993faad44f113fb37ad0ee60aef8db0d`  
		Last Modified: Mon, 22 Jun 2026 22:44:49 GMT  
		Size: 101.0 MB (101009813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945d082ad56bc9bffb53f931220fcb4c0a95aec6b2b46214e81e7a476b9aaae8`  
		Last Modified: Wed, 24 Jun 2026 09:44:23 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260619-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:474f613d3a53a16df0ecfb8e52592209a4eafd215b0263dce63ad7dbe4732af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b608ce370be4c20065838a494e9a293fa3405114e42c1a706335b252b49c38`

```dockerfile
```

-	Layers:
	-	`sha256:a849830ccdfda65734b0b0061581a9a63309d302fa688305a62ba88f8c21abef`  
		Last Modified: Wed, 24 Jun 2026 09:44:23 GMT  
		Size: 10.3 MB (10329579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6f06dead1ef1f0cf6d0a7998867ab7f791e7cab122a8a1cf383cba55ffea2b`  
		Last Modified: Wed, 24 Jun 2026 09:44:22 GMT  
		Size: 28.4 KB (28388 bytes)  
		MIME: application/vnd.in-toto+json
