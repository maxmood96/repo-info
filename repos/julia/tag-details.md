<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-alpine`](#julia1-alpine)
-	[`julia:1-alpine3.20`](#julia1-alpine320)
-	[`julia:1-alpine3.21`](#julia1-alpine321)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10.7`](#julia1107)
-	[`julia:1.10.7-bookworm`](#julia1107-bookworm)
-	[`julia:1.10.7-bullseye`](#julia1107-bullseye)
-	[`julia:1.10.7-windowsservercore`](#julia1107-windowsservercore)
-	[`julia:1.10.7-windowsservercore-1809`](#julia1107-windowsservercore-1809)
-	[`julia:1.10.7-windowsservercore-ltsc2022`](#julia1107-windowsservercore-ltsc2022)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-alpine`](#julia111-alpine)
-	[`julia:1.11-alpine3.20`](#julia111-alpine320)
-	[`julia:1.11-alpine3.21`](#julia111-alpine321)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11.2`](#julia1112)
-	[`julia:1.11.2-alpine`](#julia1112-alpine)
-	[`julia:1.11.2-alpine3.20`](#julia1112-alpine320)
-	[`julia:1.11.2-alpine3.21`](#julia1112-alpine321)
-	[`julia:1.11.2-bookworm`](#julia1112-bookworm)
-	[`julia:1.11.2-bullseye`](#julia1112-bullseye)
-	[`julia:1.11.2-windowsservercore`](#julia1112-windowsservercore)
-	[`julia:1.11.2-windowsservercore-1809`](#julia1112-windowsservercore-1809)
-	[`julia:1.11.2-windowsservercore-ltsc2022`](#julia1112-windowsservercore-ltsc2022)
-	[`julia:alpine`](#juliaalpine)
-	[`julia:alpine3.20`](#juliaalpine320)
-	[`julia:alpine3.21`](#juliaalpine321)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:d56f04472412b99cefe710d5bfcfc0c124e8b0abb03aa134ab535696831c5223
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.20`

```console
$ docker pull julia@sha256:36bdd2cff17d005def5ced39df2fce1f06f3797e6c789d07fe5cd93eb234bf72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:e764199815d9453aceae6459f4a5235ada084c9ecf6ac65c6718726bf60be959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294460117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da63cdeddf7a4b78d42adce868b0130a8cd28ecba1448b8eeb878cd7baffbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896bc82c7ec6c59f0af6e7dfeb6b1d6668aeb7a36f4958a8d79a670e4f2c809`  
		Last Modified: Wed, 08 Jan 2025 18:00:28 GMT  
		Size: 290.8 MB (290833491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cdd7c23ebe1c1c15f2284c5bd6f67b6ab00e769bf6d6b3f11927b6ce8080e`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:9ecd79dd21d9b8e165c8c341265de3b0f308fe50dc63996cfd29411eae5f1c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8132bfe87e02db14d7973f745bb4e474c438005dca92ffa9351f2dc5227e509f`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f94b43ab787e3bbdcf9f8b40787d331e15968f3aa284c4c086c21ca392488`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7e7d5a18dc1105acbf200e1eafc5480eb5b0a00aad3bee06b108acb75ff7f6`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-alpine3.21`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:b20c06f3022ac617e8fadd7c01ae1896a1bc79a766ac61d22b6efb57cb15462e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:869ee345762f49cde5b32617591f02f73174c2c5f3df594c9ed3e39d9181532d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:05ac1d180ae775520783b4447b5f952314e2d46e39007e9d16b372b89b425f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a9fe58a9097f28293e1874928b9f3d7a9cda97b9713df8b390c085e3543f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a0631cb737ad6d40b05283cc1eff54301d6c5b38d067ce0e200ba9637ee4fe`  
		Last Modified: Tue, 14 Jan 2025 22:49:43 GMT  
		Size: 2.2 MB (2222650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7a8e57ff8e3b71a4f9a1b868eb73e49e4df1156dda2a992dba73534c402e2`  
		Last Modified: Tue, 14 Jan 2025 21:39:05 GMT  
		Size: 288.5 MB (288487945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc86e66e66142fa9c8716a37ee50bbee6180deb5f4fe0a254d70c0eafc0830b`  
		Last Modified: Tue, 14 Jan 2025 22:49:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0068a9bb173de80958ff9442f8c62c6536ebd6f615113d89391f9ad4aa79a2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb598777c34951f7bceba0ddc2a05fc451f165b0c2a86064b3b5a4edb33aa311`

```dockerfile
```

-	Layers:
	-	`sha256:0761dd8b623c1cf1ba3f308981429a7885d12bcd2f9699fc8fc780fd81b15305`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46093d29ec1015772bd08b6f33ca8586a4a43342e5ba6eff5d80f5f7aa0596e`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a14cbef407db073f9fc7ebf7577ccead8e1f4809aa2f5b12452e2291c94e0b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886d2822f52bff14acfb444fd356ec20aeb5ac1f9f65310eafbe0eaae5ae6b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Wed, 15 Jan 2025 10:02:26 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ebe2f79ae438c6a9e41f24a152f26cdb5ac0cb4bf4dbabc2948f296f1d8130`  
		Last Modified: Wed, 15 Jan 2025 10:02:34 GMT  
		Size: 303.7 MB (303658631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a5d095bb4544b4ab9f706a9f42b3c5d167b7bb48e748aadd359ef54f15f10`  
		Last Modified: Wed, 15 Jan 2025 10:02:27 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:129db3061e481bdcae315987c6c6c73105591aabf8382711245989f7a00bc42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59de241fc83ec7c3d94633035f3370af8ac370fdff0aea100e7204d1ee0303ba`

```dockerfile
```

-	Layers:
	-	`sha256:5b6c1bf5c7e163f97436b1691e18afe19ce6287c3bd17b5ff774d8121593532d`  
		Last Modified: Tue, 14 Jan 2025 03:04:51 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680d468a7722b6c5d20f5251fcec541f339c9d91aee3da6287fd4dd2162bdc1`  
		Last Modified: Tue, 14 Jan 2025 03:04:50 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8014d1fbc360bbf20f436ef4b6676a4cb1f76269b2521f4ee037598b4585a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c385e2eca9546abb577d93cdb634579c2aad552d43aed2f67acde54506a62b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb262508489edb3bf552a8ace99c74836bb035af6a4e57f047b478937cbd654`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.3 MB (2328073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e1a81168c1c37ba314af2c039a9086254605bf36a19fa5dee1a3d3a8caced`  
		Last Modified: Tue, 14 Jan 2025 02:16:51 GMT  
		Size: 237.1 MB (237136285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917430375832f167acb8d4c0a254ecfc651f33f4a64827c8ed8124fadfc95d2`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:069851953b66816485680c39dc99aaa8f0336401b7a8b9898628542f17dcffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f4dcdaaa8b4068454d4c84b68e4273d26015280ebbf5984c38fb27253e049`

```dockerfile
```

-	Layers:
	-	`sha256:b582ae0dc631c6407cbe4e8ab7a328f9a737547ece1f346919e8a2386933a74d`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fade18a87176d0b2e6b623123934393d0f9f17ecae7bee2fe31c592805a9789`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:aedae46bbb77718ddc659274a6d00523ae9966f2c02b58767bb1f99020dabc69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 20:54:07 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 20:52:11 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 20:51:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Wed, 15 Jan 2025 09:13:15 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Tue, 07 Jan 2025 04:41:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Mon, 06 Jan 2025 19:49:06 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Tue, 07 Jan 2025 05:42:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Last Modified: Tue, 07 Jan 2025 06:40:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Tue, 07 Jan 2025 04:41:41 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Tue, 07 Jan 2025 01:46:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Tue, 07 Jan 2025 02:41:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Mon, 06 Jan 2025 17:46:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Mon, 06 Jan 2025 19:49:20 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Tue, 07 Jan 2025 03:41:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:ead6152a885d859cf83d3ba7194be4e4f07bbe63b83a140d28e42e1ff6b5e656
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 20:54:07 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 20:52:11 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 20:51:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Wed, 15 Jan 2025 09:13:15 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:a643b586fe3237aa1e3b85b8498eb71780a62dd93e802f026325162f3053fbbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:aac9a837df906922a4340a6c00a7b79df61544569823530b35ce1e5f097559e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3037480c5ee98533eb0b15669864b9e843a8acc2ebc67c9ca4f204ac0198968f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55b5df03cc04376fb0a788be2fb725f972110e022d592477a1ccad2788538b`  
		Last Modified: Wed, 15 Jan 2025 10:02:32 GMT  
		Size: 2.2 MB (2222645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b9988d5edf1d2e245b240c8fe1c9ec8fecd839e593d09e1508db59e8ce950`  
		Last Modified: Wed, 15 Jan 2025 02:34:42 GMT  
		Size: 175.9 MB (175895657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb0a37975db8025f32e81a3e717b83a2405bcfce346ab98530668b7c85ebabb`  
		Last Modified: Wed, 15 Jan 2025 10:03:57 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:294c6b5db1c4d27b0997b89aa867b06eb6964c2456b7401a1c923ca4b0c9b80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b88bf9d073694ea233e45e582239affd9f857b529c405b553be16b46ba8751`

```dockerfile
```

-	Layers:
	-	`sha256:74a7be86fe063c42ab0f5b1ecc059825edd73dcd2bb029add233636087ae5e29`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb04cca202779d02693c8339cec1cfea3c49817dcea8b88143d2b2c3e8fce28`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8c730d262ba8e00edc305a153b344806c0d8cb625df5af427aac0cef4b179391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0673c51f1f055362811b1b709c816c4c8fd481f983dc3c16f6395b8e52af9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Wed, 15 Jan 2025 10:02:26 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0a2d27d92a61bc9a4ead6261c01be9335fe3104de9ffb57614fa832f2ccc1`  
		Last Modified: Wed, 15 Jan 2025 10:02:35 GMT  
		Size: 177.7 MB (177651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f07fffbea1c39ed3847dbd063891bbe6e87b7f6bfc71269a488d73d5adc93d`  
		Last Modified: Wed, 15 Jan 2025 10:04:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:49afea0e98166811c93be8a8e28c44f8d3849e9bc65080c98d0f85bf6e2faa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f782e1c3ae70ab6f35994ac0437e77772d0bd357524ebdf0a3eee07d58fb3`

```dockerfile
```

-	Layers:
	-	`sha256:1ec5482662762f70d5b53a0c5639dd9b6d8e3363d3e68876b460a5689d00a429`  
		Last Modified: Tue, 14 Jan 2025 03:07:02 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d6f3d22d160c355da4ce15c196eb2df5baf6707b314e07d1c4cc6c07480e15`  
		Last Modified: Tue, 14 Jan 2025 03:07:01 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:170c925a9da9a0b982fc2c4d9aaaa503624e5562f0aead115f347320f411eac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beebdd84b2fc10ea9226ce9826470f3f72a62023bc87a3d64abe5bb9db52011`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879f31fb96b43e23c3e054f0820123765b412dc66530af4ad3588c9b5bf44e1`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.3 MB (2328064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec88cc224c3977de0a32d85d327e7840466c5b64ab35971ff90e47ae28d715b`  
		Last Modified: Tue, 14 Jan 2025 02:16:32 GMT  
		Size: 157.8 MB (157784860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47442c6195b93bb9d7b49a40f8c450fc0900ff87d96030a583287dec9607b031`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:adec2665c7cf2c7300b1ea7fc3405d27c93287d1673b4ca039fe10abb2ce402f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8112c94bd75b90229d93506219da7ca4c57d6cb71bec263d46f0eaa04a98e25c`

```dockerfile
```

-	Layers:
	-	`sha256:c216fd2acccb7d7dbf197f9e689c2a26613942aff7862c8e2030ae22caa15bd4`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3819793522831161986b2a33da4bbce69a029175059ca1ca5691cb9ed760462f`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:079eb9a75382cf1e65691ee7a837961f549e71a42f5475f72bbaaca2ffd12306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Tue, 07 Jan 2025 04:41:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Mon, 06 Jan 2025 19:49:06 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Tue, 07 Jan 2025 05:42:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Last Modified: Tue, 07 Jan 2025 06:40:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Tue, 07 Jan 2025 04:41:41 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Tue, 07 Jan 2025 01:46:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Tue, 07 Jan 2025 02:41:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Mon, 06 Jan 2025 17:46:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Mon, 06 Jan 2025 19:49:20 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Tue, 07 Jan 2025 03:41:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:bb2bc3e84f5cc89b10bf6764d626eea3f27071788bed326ec896dc70dc009db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Tue, 07 Jan 2025 01:46:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Tue, 07 Jan 2025 02:41:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Mon, 06 Jan 2025 17:46:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Mon, 06 Jan 2025 19:49:20 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Tue, 07 Jan 2025 03:41:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c8dc5bad2f3491515a7f125757486f9992622121c585cfe77945cef34b8e5d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Tue, 07 Jan 2025 04:41:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Mon, 06 Jan 2025 19:49:06 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Tue, 07 Jan 2025 05:42:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Last Modified: Tue, 07 Jan 2025 06:40:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Tue, 07 Jan 2025 04:41:41 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7`

```console
$ docker pull julia@sha256:aedae46bbb77718ddc659274a6d00523ae9966f2c02b58767bb1f99020dabc69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10.7` - linux; amd64

```console
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 20:54:07 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 20:52:11 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 20:51:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Wed, 15 Jan 2025 09:13:15 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Tue, 07 Jan 2025 04:41:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Mon, 06 Jan 2025 19:49:06 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Tue, 07 Jan 2025 05:42:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Last Modified: Tue, 07 Jan 2025 06:40:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Tue, 07 Jan 2025 04:41:41 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Tue, 07 Jan 2025 01:46:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Tue, 07 Jan 2025 02:41:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Mon, 06 Jan 2025 17:46:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Mon, 06 Jan 2025 19:49:20 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Tue, 07 Jan 2025 03:41:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-bookworm`

```console
$ docker pull julia@sha256:ead6152a885d859cf83d3ba7194be4e4f07bbe63b83a140d28e42e1ff6b5e656
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:edd8de6510b41380651a0cfce22b95b35c4da74184b445c72403d79a61128e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209820793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da4b22e31d70c27cdbc9b37d5cb06473a0aa44220fa11776bbbe8ed773f5500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0f28404f369a710bab9a7c8388f492515011cc9095e9c3e12e849397abb5f4`  
		Last Modified: Tue, 14 Jan 2025 20:54:07 GMT  
		Size: 5.7 MB (5713137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d950c86f350d07745d0403dfd6e7416bf0d520f5bb22e57a8127ee78f3689884`  
		Last Modified: Tue, 14 Jan 2025 20:52:11 GMT  
		Size: 175.9 MB (175894869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6dc88d3be5f4199dc8c192ce0db757a06af315119d62918deb33b1b735cd84`  
		Last Modified: Tue, 14 Jan 2025 20:51:55 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:83649d9658dc29386ea551f5b6a26e4a4f881e72b84af153c9de225516dce223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cceb6560d44190fbd71209922e92d21aa460129b81be0851c3eddba013f46db3`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd313d1adc26214152571b6a8361b2f047de3fbaca2fdd643fa596075ac75d`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 2.4 MB (2445483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:687f2e415413015322e2ae1220790502438bbf0a4b55874f0913fd2d7e4960a4`  
		Last Modified: Tue, 14 Jan 2025 02:20:44 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f6af94e92c3d6347eab43aadb000bb521875ef99e5ec82de1aaf5521b1016144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.2 MB (211231308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d97223e860c940f4d8d1a4a061e40dd6985221472e191b52817510ea2cbdde3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0c08dd08bd17849cf22675ca0243c698c6fe4b01fabf6a3c3d073ef52292bc`  
		Last Modified: Wed, 15 Jan 2025 09:13:15 GMT  
		Size: 177.7 MB (177651878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add6f4e4175dd49db2bde47c474a365f589850c500efe8b17e48ed1535cd756`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:98dc2724dd034ffa94dd1f0f51581ac92581d5494d620beedfd99159873e59cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2461860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8db5079d2214bbd30e0b479a0e06e399a978371ce527844283919e1810d5821f`

```dockerfile
```

-	Layers:
	-	`sha256:584938e17917b487f9f2c8b8c1c4698fd5a185b74a5efd7396891594cdeddb5e`  
		Last Modified: Tue, 14 Jan 2025 03:06:06 GMT  
		Size: 2.4 MB (2444527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58528a32f89e6930ab0f01a38d3579676a8c42a3c1de8037d4691f810c72e23d`  
		Last Modified: Tue, 14 Jan 2025 03:06:05 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a225d5ce3452efef8a6a3c7b3128752f37432714f470939463dd9bfd85025b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192844952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9966ac739b39d1a45e05398b35cfbdf47a58d4b97757c26b4c312ab20ba21d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfacadf125ebfe614f9d429c8b5bdf6d0d903c4df91e2da95d4132ce3c3a82e2`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 5.9 MB (5872050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dba39a827ee7f55656de9c241021310212ca40705cd8f8c9bec6c14d9880c7`  
		Last Modified: Tue, 14 Jan 2025 02:32:01 GMT  
		Size: 157.8 MB (157784935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388237bea775ed66dc6f643bb7d0c724ec9defae5550008ac32ad5e0d2e7ca22`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b0b3fbabded9d034923cc5379cb00d41b9b80829dba5100bcb7524115879ea3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2459756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e274e9ccf1d8fb36d5d92f737c19bff89fdcba539fa03dd899174db0d5039333`

```dockerfile
```

-	Layers:
	-	`sha256:cde977fe1eb34823bbb2bb31c87ddd7596095cdc36d134a6fc3f862b1eee9aef`  
		Last Modified: Tue, 14 Jan 2025 02:31:57 GMT  
		Size: 2.4 MB (2442576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bea311a8209b26d03597c5b41d6fda1ee44775d18c496c8acdad213c081e776a`  
		Last Modified: Tue, 14 Jan 2025 02:31:56 GMT  
		Size: 17.2 KB (17180 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:417e5fc281dfa44fc541d6df19d69af1c650dc06aaa978e25360cfb85f3351b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193787835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3f23264d7289f18ce257bee838033b1a6a2a4b70f0f5311791be9606346526`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5a111a086bbf1d30ef24a905695854d18360157ff9692f11169c90ccc428e`  
		Last Modified: Tue, 14 Jan 2025 02:59:02 GMT  
		Size: 155.5 MB (155493289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d4d0b667db150b41b9760574e56cdd03830247e5c902dcfc7a95b1cf9e8c0c`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9858b4a4e5491fda48000243dcbe4017e8e5456af0147070065871ee8e1dddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2e3bd039358880b6e19c014c81ccb9785636c895bcfc85489dcb6189d0bc2f`

```dockerfile
```

-	Layers:
	-	`sha256:85ff17fb46e315f1e821f7e0f86f3c00a6f80fb0320db89cb4eb6402f5b194de`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 2.4 MB (2448660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13be94c786bf7ce3dbe980dc608d497c828bda708eb0849cb3ef08c0ca18eabe`  
		Last Modified: Tue, 14 Jan 2025 02:58:58 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-bullseye`

```console
$ docker pull julia@sha256:a643b586fe3237aa1e3b85b8498eb71780a62dd93e802f026325162f3053fbbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:aac9a837df906922a4340a6c00a7b79df61544569823530b35ce1e5f097559e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3037480c5ee98533eb0b15669864b9e843a8acc2ebc67c9ca4f204ac0198968f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55b5df03cc04376fb0a788be2fb725f972110e022d592477a1ccad2788538b`  
		Last Modified: Wed, 15 Jan 2025 10:02:32 GMT  
		Size: 2.2 MB (2222645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17b9988d5edf1d2e245b240c8fe1c9ec8fecd839e593d09e1508db59e8ce950`  
		Last Modified: Wed, 15 Jan 2025 02:34:42 GMT  
		Size: 175.9 MB (175895657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb0a37975db8025f32e81a3e717b83a2405bcfce346ab98530668b7c85ebabb`  
		Last Modified: Wed, 15 Jan 2025 10:03:57 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:294c6b5db1c4d27b0997b89aa867b06eb6964c2456b7401a1c923ca4b0c9b80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b88bf9d073694ea233e45e582239affd9f857b529c405b553be16b46ba8751`

```dockerfile
```

-	Layers:
	-	`sha256:74a7be86fe063c42ab0f5b1ecc059825edd73dcd2bb029add233636087ae5e29`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 2.7 MB (2713173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb04cca202779d02693c8339cec1cfea3c49817dcea8b88143d2b2c3e8fce28`  
		Last Modified: Tue, 14 Jan 2025 02:20:48 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8c730d262ba8e00edc305a153b344806c0d8cb625df5af427aac0cef4b179391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208607436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0673c51f1f055362811b1b709c816c4c8fd481f983dc3c16f6395b8e52af9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Wed, 15 Jan 2025 10:02:26 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0a2d27d92a61bc9a4ead6261c01be9335fe3104de9ffb57614fa832f2ccc1`  
		Last Modified: Wed, 15 Jan 2025 10:02:35 GMT  
		Size: 177.7 MB (177651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f07fffbea1c39ed3847dbd063891bbe6e87b7f6bfc71269a488d73d5adc93d`  
		Last Modified: Wed, 15 Jan 2025 10:04:04 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:49afea0e98166811c93be8a8e28c44f8d3849e9bc65080c98d0f85bf6e2faa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2728902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f782e1c3ae70ab6f35994ac0437e77772d0bd357524ebdf0a3eee07d58fb3`

```dockerfile
```

-	Layers:
	-	`sha256:1ec5482662762f70d5b53a0c5639dd9b6d8e3363d3e68876b460a5689d00a429`  
		Last Modified: Tue, 14 Jan 2025 03:07:02 GMT  
		Size: 2.7 MB (2712181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56d6f3d22d160c355da4ce15c196eb2df5baf6707b314e07d1c4cc6c07480e15`  
		Last Modified: Tue, 14 Jan 2025 03:07:01 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:170c925a9da9a0b982fc2c4d9aaaa503624e5562f0aead115f347320f411eac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191292320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beebdd84b2fc10ea9226ce9826470f3f72a62023bc87a3d64abe5bb9db52011`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 27 Nov 2024 00:59:11 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 27 Nov 2024 00:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 27 Nov 2024 00:59:11 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 27 Nov 2024 00:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.7-linux-x86_64.tar.gz'; 			sha256='21b2c69806aacf191d7c81806c7d9918bddab30c7b5b8d4251389c3abe274334'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.7-linux-aarch64.tar.gz'; 			sha256='93bf1b113f297c817310f77d1edce4ab9dcbf49432489cb8df09afbf93d1e5a0'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.7-linux-i686.tar.gz'; 			sha256='3e5afefd8a77d1e96b7037bfcd23def8f8993e3d0ca8408fffb292fa60a25cd0'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.7-linux-ppc64le.tar.gz'; 			sha256='6c8b3d4b05a5620efa68abc146c267e198dc0cd71a2c7bc02662fa0a424f679c'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Nov 2024 00:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Nov 2024 00:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879f31fb96b43e23c3e054f0820123765b412dc66530af4ad3588c9b5bf44e1`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.3 MB (2328064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec88cc224c3977de0a32d85d327e7840466c5b64ab35971ff90e47ae28d715b`  
		Last Modified: Tue, 14 Jan 2025 02:16:32 GMT  
		Size: 157.8 MB (157784860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47442c6195b93bb9d7b49a40f8c450fc0900ff87d96030a583287dec9607b031`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.7-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:adec2665c7cf2c7300b1ea7fc3405d27c93287d1673b4ca039fe10abb2ce402f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8112c94bd75b90229d93506219da7ca4c57d6cb71bec263d46f0eaa04a98e25c`

```dockerfile
```

-	Layers:
	-	`sha256:c216fd2acccb7d7dbf197f9e689c2a26613942aff7862c8e2030ae22caa15bd4`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 2.7 MB (2710282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3819793522831161986b2a33da4bbce69a029175059ca1ca5691cb9ed760462f`  
		Last Modified: Tue, 14 Jan 2025 02:16:28 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.7-windowsservercore`

```console
$ docker pull julia@sha256:079eb9a75382cf1e65691ee7a837961f549e71a42f5475f72bbaaca2ffd12306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10.7-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Tue, 07 Jan 2025 04:41:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Mon, 06 Jan 2025 19:49:06 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Tue, 07 Jan 2025 05:42:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Last Modified: Tue, 07 Jan 2025 06:40:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Tue, 07 Jan 2025 04:41:41 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.7-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Tue, 07 Jan 2025 01:46:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Tue, 07 Jan 2025 02:41:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Mon, 06 Jan 2025 17:46:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Mon, 06 Jan 2025 19:49:20 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Tue, 07 Jan 2025 03:41:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:bb2bc3e84f5cc89b10bf6764d626eea3f27071788bed326ec896dc70dc009db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.10.7-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:6fd48028e26d3e7b9d5d569601f1119da7acee350d3cb02b5931bf2bf9a82348
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203383339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efa9a0b90887594deb2b9614a307dfd7de3c275121d217ac28fcf8504478e08`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:37:03 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:38:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9557c86267a346d70a76c911288e910d09a34a18f276b523bc2dc52a4e19dec2`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c358c54c4a8884495b0de12b39bae277e5156994ab9b86d8545331f9c0429b`  
		Last Modified: Tue, 07 Jan 2025 01:46:00 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaae011b7bc6768c2ee2351f6caec22692d76a95762dd9e4d1a9ac3c118eea56`  
		Last Modified: Tue, 07 Jan 2025 02:41:40 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec9d76031ae2b5402258919ae14d0b6f31ec3e5d71185a01a3618269c7454ca`  
		Last Modified: Mon, 06 Jan 2025 17:46:50 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbb21f52efa9de9cc676636101546f3d4066162e3393b4a83661307b01c9b73`  
		Last Modified: Mon, 06 Jan 2025 19:49:20 GMT  
		Size: 189.2 MB (189206644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000e0197976c3cf355755645ab946d9f5c748efc49fcc3cfd522b86d957f1db8`  
		Last Modified: Tue, 07 Jan 2025 03:41:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c8dc5bad2f3491515a7f125757486f9992622121c585cfe77945cef34b8e5d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.10.7-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:67f1450b2c6c5b228aaf76465850a15fe2ce1965868fbdae9156e3b9855a7802
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442946290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a754b0ee25001c1d373937738c31ad67d1919ba65a3a8c2c66541a6521d3a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:38:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:38:37 GMT
ENV JULIA_VERSION=1.10.7
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.7-win64.exe
# Wed, 11 Dec 2024 20:38:38 GMT
ENV JULIA_SHA256=51689d4e608fb78468ffabf55fd72896c3f3d84770cf58accb87cd0a57e9cbb8
# Wed, 11 Dec 2024 20:39:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:39:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9784d6ef9750850e70db0a9708b578593c771be826c9d5ea59e1baa59eb1a351`  
		Last Modified: Tue, 07 Jan 2025 04:41:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b71b6f52b610f2554e301356ada09ef971e0f0d29d81e28e8f4c64b45d0fb2`  
		Last Modified: Mon, 06 Jan 2025 19:49:06 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a4af9945ddd5c3cbbc589f898bb1ff96d873e219505f1cbda46cf823567213`  
		Last Modified: Tue, 07 Jan 2025 05:42:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e669871576de36c202b45876ff0f2991f17ee2d30a0db66a08aeca13607f8d6`  
		Last Modified: Tue, 07 Jan 2025 06:40:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360f5b87906b9505cda487f2b333a9158b50033836df72359487f512b465aae`  
		Last Modified: Tue, 07 Jan 2025 04:41:41 GMT  
		Size: 189.1 MB (189066206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c46d5150ee9182ffe3ac8ec36f1400e4751d241e8e4a35fd6b3d4968801df`  
		Last Modified: Tue, 07 Jan 2025 07:43:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:d56f04472412b99cefe710d5bfcfc0c124e8b0abb03aa134ab535696831c5223
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-alpine`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11-alpine` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-alpine3.20`

```console
$ docker pull julia@sha256:36bdd2cff17d005def5ced39df2fce1f06f3797e6c789d07fe5cd93eb234bf72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:e764199815d9453aceae6459f4a5235ada084c9ecf6ac65c6718726bf60be959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294460117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da63cdeddf7a4b78d42adce868b0130a8cd28ecba1448b8eeb878cd7baffbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896bc82c7ec6c59f0af6e7dfeb6b1d6668aeb7a36f4958a8d79a670e4f2c809`  
		Last Modified: Wed, 08 Jan 2025 18:00:28 GMT  
		Size: 290.8 MB (290833491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cdd7c23ebe1c1c15f2284c5bd6f67b6ab00e769bf6d6b3f11927b6ce8080e`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:9ecd79dd21d9b8e165c8c341265de3b0f308fe50dc63996cfd29411eae5f1c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8132bfe87e02db14d7973f745bb4e474c438005dca92ffa9351f2dc5227e509f`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f94b43ab787e3bbdcf9f8b40787d331e15968f3aa284c4c086c21ca392488`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7e7d5a18dc1105acbf200e1eafc5480eb5b0a00aad3bee06b108acb75ff7f6`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-alpine3.21`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:b20c06f3022ac617e8fadd7c01ae1896a1bc79a766ac61d22b6efb57cb15462e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:869ee345762f49cde5b32617591f02f73174c2c5f3df594c9ed3e39d9181532d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:05ac1d180ae775520783b4447b5f952314e2d46e39007e9d16b372b89b425f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a9fe58a9097f28293e1874928b9f3d7a9cda97b9713df8b390c085e3543f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a0631cb737ad6d40b05283cc1eff54301d6c5b38d067ce0e200ba9637ee4fe`  
		Last Modified: Tue, 14 Jan 2025 22:49:43 GMT  
		Size: 2.2 MB (2222650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7a8e57ff8e3b71a4f9a1b868eb73e49e4df1156dda2a992dba73534c402e2`  
		Last Modified: Tue, 14 Jan 2025 21:39:05 GMT  
		Size: 288.5 MB (288487945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc86e66e66142fa9c8716a37ee50bbee6180deb5f4fe0a254d70c0eafc0830b`  
		Last Modified: Tue, 14 Jan 2025 22:49:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0068a9bb173de80958ff9442f8c62c6536ebd6f615113d89391f9ad4aa79a2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb598777c34951f7bceba0ddc2a05fc451f165b0c2a86064b3b5a4edb33aa311`

```dockerfile
```

-	Layers:
	-	`sha256:0761dd8b623c1cf1ba3f308981429a7885d12bcd2f9699fc8fc780fd81b15305`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46093d29ec1015772bd08b6f33ca8586a4a43342e5ba6eff5d80f5f7aa0596e`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a14cbef407db073f9fc7ebf7577ccead8e1f4809aa2f5b12452e2291c94e0b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886d2822f52bff14acfb444fd356ec20aeb5ac1f9f65310eafbe0eaae5ae6b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Wed, 15 Jan 2025 10:02:26 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ebe2f79ae438c6a9e41f24a152f26cdb5ac0cb4bf4dbabc2948f296f1d8130`  
		Last Modified: Wed, 15 Jan 2025 10:02:34 GMT  
		Size: 303.7 MB (303658631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a5d095bb4544b4ab9f706a9f42b3c5d167b7bb48e748aadd359ef54f15f10`  
		Last Modified: Wed, 15 Jan 2025 10:02:27 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:129db3061e481bdcae315987c6c6c73105591aabf8382711245989f7a00bc42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59de241fc83ec7c3d94633035f3370af8ac370fdff0aea100e7204d1ee0303ba`

```dockerfile
```

-	Layers:
	-	`sha256:5b6c1bf5c7e163f97436b1691e18afe19ce6287c3bd17b5ff774d8121593532d`  
		Last Modified: Tue, 14 Jan 2025 03:04:51 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680d468a7722b6c5d20f5251fcec541f339c9d91aee3da6287fd4dd2162bdc1`  
		Last Modified: Tue, 14 Jan 2025 03:04:50 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8014d1fbc360bbf20f436ef4b6676a4cb1f76269b2521f4ee037598b4585a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c385e2eca9546abb577d93cdb634579c2aad552d43aed2f67acde54506a62b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb262508489edb3bf552a8ace99c74836bb035af6a4e57f047b478937cbd654`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.3 MB (2328073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e1a81168c1c37ba314af2c039a9086254605bf36a19fa5dee1a3d3a8caced`  
		Last Modified: Tue, 14 Jan 2025 02:16:51 GMT  
		Size: 237.1 MB (237136285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917430375832f167acb8d4c0a254ecfc651f33f4a64827c8ed8124fadfc95d2`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:069851953b66816485680c39dc99aaa8f0336401b7a8b9898628542f17dcffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f4dcdaaa8b4068454d4c84b68e4273d26015280ebbf5984c38fb27253e049`

```dockerfile
```

-	Layers:
	-	`sha256:b582ae0dc631c6407cbe4e8ab7a328f9a737547ece1f346919e8a2386933a74d`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fade18a87176d0b2e6b623123934393d0f9f17ecae7bee2fe31c592805a9789`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2`

```console
$ docker pull julia@sha256:d56f04472412b99cefe710d5bfcfc0c124e8b0abb03aa134ab535696831c5223
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11.2` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.2` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2-alpine`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11.2-alpine` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-alpine3.20`

```console
$ docker pull julia@sha256:36bdd2cff17d005def5ced39df2fce1f06f3797e6c789d07fe5cd93eb234bf72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11.2-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:e764199815d9453aceae6459f4a5235ada084c9ecf6ac65c6718726bf60be959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294460117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da63cdeddf7a4b78d42adce868b0130a8cd28ecba1448b8eeb878cd7baffbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896bc82c7ec6c59f0af6e7dfeb6b1d6668aeb7a36f4958a8d79a670e4f2c809`  
		Last Modified: Wed, 08 Jan 2025 18:00:28 GMT  
		Size: 290.8 MB (290833491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cdd7c23ebe1c1c15f2284c5bd6f67b6ab00e769bf6d6b3f11927b6ce8080e`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:9ecd79dd21d9b8e165c8c341265de3b0f308fe50dc63996cfd29411eae5f1c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8132bfe87e02db14d7973f745bb4e474c438005dca92ffa9351f2dc5227e509f`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f94b43ab787e3bbdcf9f8b40787d331e15968f3aa284c4c086c21ca392488`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7e7d5a18dc1105acbf200e1eafc5480eb5b0a00aad3bee06b108acb75ff7f6`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-alpine3.21`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.11.2-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-bookworm`

```console
$ docker pull julia@sha256:b20c06f3022ac617e8fadd7c01ae1896a1bc79a766ac61d22b6efb57cb15462e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.2-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bookworm` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-bullseye`

```console
$ docker pull julia@sha256:869ee345762f49cde5b32617591f02f73174c2c5f3df594c9ed3e39d9181532d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.2-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:05ac1d180ae775520783b4447b5f952314e2d46e39007e9d16b372b89b425f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a9fe58a9097f28293e1874928b9f3d7a9cda97b9713df8b390c085e3543f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a0631cb737ad6d40b05283cc1eff54301d6c5b38d067ce0e200ba9637ee4fe`  
		Last Modified: Tue, 14 Jan 2025 22:49:43 GMT  
		Size: 2.2 MB (2222650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7a8e57ff8e3b71a4f9a1b868eb73e49e4df1156dda2a992dba73534c402e2`  
		Last Modified: Tue, 14 Jan 2025 21:39:05 GMT  
		Size: 288.5 MB (288487945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc86e66e66142fa9c8716a37ee50bbee6180deb5f4fe0a254d70c0eafc0830b`  
		Last Modified: Tue, 14 Jan 2025 22:49:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0068a9bb173de80958ff9442f8c62c6536ebd6f615113d89391f9ad4aa79a2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb598777c34951f7bceba0ddc2a05fc451f165b0c2a86064b3b5a4edb33aa311`

```dockerfile
```

-	Layers:
	-	`sha256:0761dd8b623c1cf1ba3f308981429a7885d12bcd2f9699fc8fc780fd81b15305`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46093d29ec1015772bd08b6f33ca8586a4a43342e5ba6eff5d80f5f7aa0596e`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a14cbef407db073f9fc7ebf7577ccead8e1f4809aa2f5b12452e2291c94e0b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886d2822f52bff14acfb444fd356ec20aeb5ac1f9f65310eafbe0eaae5ae6b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Wed, 15 Jan 2025 10:02:26 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ebe2f79ae438c6a9e41f24a152f26cdb5ac0cb4bf4dbabc2948f296f1d8130`  
		Last Modified: Wed, 15 Jan 2025 10:02:34 GMT  
		Size: 303.7 MB (303658631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a5d095bb4544b4ab9f706a9f42b3c5d167b7bb48e748aadd359ef54f15f10`  
		Last Modified: Wed, 15 Jan 2025 10:02:27 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:129db3061e481bdcae315987c6c6c73105591aabf8382711245989f7a00bc42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59de241fc83ec7c3d94633035f3370af8ac370fdff0aea100e7204d1ee0303ba`

```dockerfile
```

-	Layers:
	-	`sha256:5b6c1bf5c7e163f97436b1691e18afe19ce6287c3bd17b5ff774d8121593532d`  
		Last Modified: Tue, 14 Jan 2025 03:04:51 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680d468a7722b6c5d20f5251fcec541f339c9d91aee3da6287fd4dd2162bdc1`  
		Last Modified: Tue, 14 Jan 2025 03:04:50 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.2-bullseye` - linux; 386

```console
$ docker pull julia@sha256:8014d1fbc360bbf20f436ef4b6676a4cb1f76269b2521f4ee037598b4585a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c385e2eca9546abb577d93cdb634579c2aad552d43aed2f67acde54506a62b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb262508489edb3bf552a8ace99c74836bb035af6a4e57f047b478937cbd654`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.3 MB (2328073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e1a81168c1c37ba314af2c039a9086254605bf36a19fa5dee1a3d3a8caced`  
		Last Modified: Tue, 14 Jan 2025 02:16:51 GMT  
		Size: 237.1 MB (237136285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917430375832f167acb8d4c0a254ecfc651f33f4a64827c8ed8124fadfc95d2`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.2-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:069851953b66816485680c39dc99aaa8f0336401b7a8b9898628542f17dcffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f4dcdaaa8b4068454d4c84b68e4273d26015280ebbf5984c38fb27253e049`

```dockerfile
```

-	Layers:
	-	`sha256:b582ae0dc631c6407cbe4e8ab7a328f9a737547ece1f346919e8a2386933a74d`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fade18a87176d0b2e6b623123934393d0f9f17ecae7bee2fe31c592805a9789`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.2-windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11.2-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.2-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2-windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:1.11.2-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.2-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1.11.2-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.20`

```console
$ docker pull julia@sha256:36bdd2cff17d005def5ced39df2fce1f06f3797e6c789d07fe5cd93eb234bf72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:e764199815d9453aceae6459f4a5235ada084c9ecf6ac65c6718726bf60be959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294460117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da63cdeddf7a4b78d42adce868b0130a8cd28ecba1448b8eeb878cd7baffbbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["/bin/sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7896bc82c7ec6c59f0af6e7dfeb6b1d6668aeb7a36f4958a8d79a670e4f2c809`  
		Last Modified: Wed, 08 Jan 2025 18:00:28 GMT  
		Size: 290.8 MB (290833491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75cdd7c23ebe1c1c15f2284c5bd6f67b6ab00e769bf6d6b3f11927b6ce8080e`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:9ecd79dd21d9b8e165c8c341265de3b0f308fe50dc63996cfd29411eae5f1c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 KB (85502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8132bfe87e02db14d7973f745bb4e474c438005dca92ffa9351f2dc5227e509f`

```dockerfile
```

-	Layers:
	-	`sha256:cf1f94b43ab787e3bbdcf9f8b40787d331e15968f3aa284c4c086c21ca392488`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 72.9 KB (72926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c7e7d5a18dc1105acbf200e1eafc5480eb5b0a00aad3bee06b108acb75ff7f6`  
		Last Modified: Wed, 08 Jan 2025 18:00:24 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:alpine3.21`

```console
$ docker pull julia@sha256:2e3ff4e7943e8e8f65c2043a901d1baf8ea5766b49938df407e6bc282889e3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:5fcab783236348a169491521389ff80176d2040d1e44204ef87f324c42e334a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294476302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8aa12b2f61512eb496edf0163cc5d53f90e4cf2815f543db14b5cecc92404a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 13 Dec 2024 00:46:18 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 13 Dec 2024 00:46:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 13 Dec 2024 00:46:18 GMT
ENV JULIA_VERSION=1.11.2
# Fri, 13 Dec 2024 00:46:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.11/julia-1.11.2-musl-x86_64.tar.gz'; 			sha256='dc7d2ec533c33f385683bad892d09c9f09f124061fa00ab7e4dd2e0912d55c19'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Dec 2024 00:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Dec 2024 00:46:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e7fff34a5418d7b7055c68413d313f6dca243fb28b598580ea870f331725c2`  
		Last Modified: Wed, 15 Jan 2025 04:13:27 GMT  
		Size: 290.8 MB (290834218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2e70e76275cec80e8c298b317dde93b72048d0c198b5d333f5919ebd5e711e`  
		Last Modified: Wed, 15 Jan 2025 04:13:18 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:26fa353dee935ea6460ec20653a22294aee58eea56136aa67fbbcc8e1ae502dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 KB (93646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59372d6aec795017dbc661b410b7ac3eafebe8a9fde7a4a6e0bfbedafd16adc`

```dockerfile
```

-	Layers:
	-	`sha256:d0c38041a4aedf679503117d6c211d1c5adadbb895719e994562307d52bf96ad`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37dd4dc7d32af19663e442310c11eab0abe70babf829f31d02628eefc2d72c73`  
		Last Modified: Wed, 08 Jan 2025 18:01:16 GMT  
		Size: 13.8 KB (13788 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bookworm`

```console
$ docker pull julia@sha256:b20c06f3022ac617e8fadd7c01ae1896a1bc79a766ac61d22b6efb57cb15462e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:869ee345762f49cde5b32617591f02f73174c2c5f3df594c9ed3e39d9181532d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:05ac1d180ae775520783b4447b5f952314e2d46e39007e9d16b372b89b425f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (320963628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a9fe58a9097f28293e1874928b9f3d7a9cda97b9713df8b390c085e3543f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a0631cb737ad6d40b05283cc1eff54301d6c5b38d067ce0e200ba9637ee4fe`  
		Last Modified: Tue, 14 Jan 2025 22:49:43 GMT  
		Size: 2.2 MB (2222650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda7a8e57ff8e3b71a4f9a1b868eb73e49e4df1156dda2a992dba73534c402e2`  
		Last Modified: Tue, 14 Jan 2025 21:39:05 GMT  
		Size: 288.5 MB (288487945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc86e66e66142fa9c8716a37ee50bbee6180deb5f4fe0a254d70c0eafc0830b`  
		Last Modified: Tue, 14 Jan 2025 22:49:42 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:0068a9bb173de80958ff9442f8c62c6536ebd6f615113d89391f9ad4aa79a2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2729776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb598777c34951f7bceba0ddc2a05fc451f165b0c2a86064b3b5a4edb33aa311`

```dockerfile
```

-	Layers:
	-	`sha256:0761dd8b623c1cf1ba3f308981429a7885d12bcd2f9699fc8fc780fd81b15305`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 2.7 MB (2712546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a46093d29ec1015772bd08b6f33ca8586a4a43342e5ba6eff5d80f5f7aa0596e`  
		Last Modified: Tue, 14 Jan 2025 02:20:50 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a14cbef407db073f9fc7ebf7577ccead8e1f4809aa2f5b12452e2291c94e0b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334614198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886d2822f52bff14acfb444fd356ec20aeb5ac1f9f65310eafbe0eaae5ae6b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35ba9e296c53b7e882a6fba6d9ff8c72398e380d38de500e5effd7f2fb92285`  
		Last Modified: Wed, 15 Jan 2025 10:02:26 GMT  
		Size: 2.2 MB (2210283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ebe2f79ae438c6a9e41f24a152f26cdb5ac0cb4bf4dbabc2948f296f1d8130`  
		Last Modified: Wed, 15 Jan 2025 10:02:34 GMT  
		Size: 303.7 MB (303658631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633a5d095bb4544b4ab9f706a9f42b3c5d167b7bb48e748aadd359ef54f15f10`  
		Last Modified: Wed, 15 Jan 2025 10:02:27 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:129db3061e481bdcae315987c6c6c73105591aabf8382711245989f7a00bc42b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2730158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59de241fc83ec7c3d94633035f3370af8ac370fdff0aea100e7204d1ee0303ba`

```dockerfile
```

-	Layers:
	-	`sha256:5b6c1bf5c7e163f97436b1691e18afe19ce6287c3bd17b5ff774d8121593532d`  
		Last Modified: Tue, 14 Jan 2025 03:04:51 GMT  
		Size: 2.7 MB (2712809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5680d468a7722b6c5d20f5251fcec541f339c9d91aee3da6287fd4dd2162bdc1`  
		Last Modified: Tue, 14 Jan 2025 03:04:50 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:8014d1fbc360bbf20f436ef4b6676a4cb1f76269b2521f4ee037598b4585a907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270643755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c385e2eca9546abb577d93cdb634579c2aad552d43aed2f67acde54506a62b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb262508489edb3bf552a8ace99c74836bb035af6a4e57f047b478937cbd654`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.3 MB (2328073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e1a81168c1c37ba314af2c039a9086254605bf36a19fa5dee1a3d3a8caced`  
		Last Modified: Tue, 14 Jan 2025 02:16:51 GMT  
		Size: 237.1 MB (237136285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917430375832f167acb8d4c0a254ecfc651f33f4a64827c8ed8124fadfc95d2`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:069851953b66816485680c39dc99aaa8f0336401b7a8b9898628542f17dcffd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6f4dcdaaa8b4068454d4c84b68e4273d26015280ebbf5984c38fb27253e049`

```dockerfile
```

-	Layers:
	-	`sha256:b582ae0dc631c6407cbe4e8ab7a328f9a737547ece1f346919e8a2386933a74d`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 2.7 MB (2709645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fade18a87176d0b2e6b623123934393d0f9f17ecae7bee2fe31c592805a9789`  
		Last Modified: Tue, 14 Jan 2025 02:16:45 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:d56f04472412b99cefe710d5bfcfc0c124e8b0abb03aa134ab535696831c5223
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:10c26cb0015ed2fb75de18d6b94cb621a48dd6bd33c6be8eb0fdcad4ef9c6d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322414206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a735412364b7eccdc7793962069b4bbff771d27ee7fd07ba344f572d93adafdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd7480e6a46ca5189534a9d28d0d61dfca1c6d094a33355d29fbdbf2b9196f`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 5.7 MB (5713150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d66e61533e2d2814daf0a0994d5b37281d839f99c7c2f4d96262b866ea68e`  
		Last Modified: Tue, 14 Jan 2025 21:15:21 GMT  
		Size: 288.5 MB (288488268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f9ffa2139f9df73e31ac48d7ac638d2b06be5813897a65497e8aa8d0e44d9`  
		Last Modified: Tue, 14 Jan 2025 20:59:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:2c042d286e12ca351e8fd4fd3181b8cd0225fe83f28fd7d569b7ed5347308546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131d0fc54763322f82c445f33149da14d1a02c028f4888a62eca175c84e3c4f7`

```dockerfile
```

-	Layers:
	-	`sha256:9d1532eb0617ad4ac587b939c29a942b5b4d8927a31922065ce52b28ccf292dd`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 2.4 MB (2445438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece714138ce3f0bb985dda002083e1ab0b46cb1ea8b68e7577a2f529c1cae83a`  
		Last Modified: Tue, 14 Jan 2025 02:21:18 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:3f5f06f492e9c74aac5523be7bdaf7ed71f2835dc400371cecc1045ab3e8ca8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337238704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d39118f9e4040d36e8979e1fbdfd171777dc9bd717e7c212cdb49d0d8297a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3edc3d5f07a51a8090abe702956bd78d8336c3e7d1e181624aa8fffdda44ba`  
		Last Modified: Wed, 15 Jan 2025 07:54:43 GMT  
		Size: 5.5 MB (5538028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b66cfa0111c5566a018bbd6622362b4cd01ad31c26df85770da7d05c6efc4ce`  
		Last Modified: Wed, 15 Jan 2025 07:54:52 GMT  
		Size: 303.7 MB (303659274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf7a61217dca81b2c700a133712a18cd3c8a04902f6ea7f4d45e0092c618b0`  
		Last Modified: Wed, 15 Jan 2025 09:13:10 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:d10d396f681ade061c29a6d2c0d33dcd43f5651ec084bd2248a54fcf95455260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a038cd700a288d0cc2d0555a32f2232121890b4ab92bd20b4bab938bbe53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4e997be8cea3850678019a63fb2ea80ec0ad2d9c00528eab19612ca36d10a47`  
		Last Modified: Tue, 14 Jan 2025 03:02:35 GMT  
		Size: 2.4 MB (2445761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:264b199697d44ed7d2e1007b4f4db44dedb0d204439ba5e856abe43336340801`  
		Last Modified: Tue, 14 Jan 2025 03:02:34 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:a300594350c7a761f1cacceed0537e53b7e8c4f8558c3d2ad419dc8146018c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272197322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c3e1d54a98051dbdfdf8e06a304cc776ed500b248f26b9a1107e65370057ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 20:35:48 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf705824c621eec17811c6e844d7d18b3f5fa3307b8bf955255101c01e32387`  
		Last Modified: Tue, 14 Jan 2025 02:16:43 GMT  
		Size: 5.9 MB (5872072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0341ff305ea3d788dc80c866ebe87215ee4e99054ead2a4cc9c9122125cd39e`  
		Last Modified: Tue, 14 Jan 2025 02:16:48 GMT  
		Size: 237.1 MB (237137283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8726d92b5bc4dd5ba69f17a0f5cbc07da115066fa1aa92c3ba7d6925c53e17`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:147cacfa03d49a789a584af335a52d5acbfe29c4022da3ceef37f33ecb1b25f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2821097ebe80f89f1d89422fdd3d62bcdde6dadea4c59a31b9b955d7c21eee2e`

```dockerfile
```

-	Layers:
	-	`sha256:48673f71a21a457b124d33f4bf6539b5b153eaf6ba88dac14e6b766b79e10995`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 2.4 MB (2442511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b812cd39381ce2c11c92889b4b5758a9e54d6789bc145fc80793e1aeac0c5ddb`  
		Last Modified: Tue, 14 Jan 2025 02:16:42 GMT  
		Size: 18.3 KB (18343 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:aa08cc44685439dbb1cf845618e5f35e4c870203b48c9fffc4005c940a930e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286222876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ee6652f9438cdcd9e2fe3c8642bae0790c8326577157bdb16d49650de8a235`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 02 Dec 2024 18:59:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 02 Dec 2024 18:59:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 02 Dec 2024 18:59:14 GMT
ENV JULIA_VERSION=1.11.2
# Mon, 02 Dec 2024 18:59:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.2-linux-x86_64.tar.gz'; 			sha256='8a372ad262d4d4d55a1044f4fe3bce7c9a4a3ce8c513d2470e58e8071eecd476'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.2-linux-aarch64.tar.gz'; 			sha256='0346e6d65852a3b73ced2c80c40f5a8cf38e7048d001cd57d3d1dd9efb2f6641'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.2-linux-i686.tar.gz'; 			sha256='a0b6e1e3a017c3db142f4c928006617870389d5f67c43adc4d0681b3bcd6c528'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.2-linux-ppc64le.tar.gz'; 			sha256='953829671af91de7002fffaec93ec8b40a063e84ad048a854f722f3cf4f76d18'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 02 Dec 2024 18:59:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 02 Dec 2024 18:59:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebdbe5b710df7d76fd413cf6229eabb5074a6a7152a0de81bad24cda5d7896`  
		Last Modified: Tue, 14 Jan 2025 02:57:01 GMT  
		Size: 6.2 MB (6249328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21850e380698aa440758091ab84014f2b933e8c59b483f8ac327a378dd4978f2`  
		Last Modified: Tue, 14 Jan 2025 02:57:06 GMT  
		Size: 247.9 MB (247928333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb4c1b04df72ed3cd80927dc1bfa0ad1dc2ec974ef54529c427bd5c54e6c8a5`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:46cf456d343be8f38b9826631030653076d5e336d5887284ae1b9659ff9670e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15150cafce13a56b83d12670825e875d95397a93ce6c6dc48863f875de9950c7`

```dockerfile
```

-	Layers:
	-	`sha256:274dd869f560c100303f986553cf044f877b284b8ffd6695ef3acd526e937792`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 2.4 MB (2449870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa92a15c74d889eaaee2213845473c2e6cedc51a4ed919dd60d81c242842683`  
		Last Modified: Tue, 14 Jan 2025 02:57:00 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:6504fe3cd8d166765a3b4071b7a72b5afd60a7e6b9dd08d669501859e3b75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:5b6c8f86646a14cc668c90bb9e5b4d13b0c18ccad74b5d74139640027a4fe3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull julia@sha256:fb40c006b065c0eb477e100f456b2f283d7c055075c7788fbdc786854537d381
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2298657293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34ef53bdca092ee793dcab87c91d3bc3f44afb71f18398c861e783791c7f01a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:35:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:35:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:35:56 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:37:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:37:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Fri, 13 Dec 2024 16:27:08 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe79962697ceb000e661dee639a10518b060d9421e3764c88852b377d23c35b`  
		Last Modified: Thu, 02 Jan 2025 15:34:49 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733d0ff8723a9b29101d674127a09be655987875f76784731805db4b1c0f03f1`  
		Last Modified: Tue, 07 Jan 2025 08:40:47 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede60c5f6b2538af0eab6b9a6107470f22f55ca844903b1e97ef6ec964f6bf91`  
		Last Modified: Mon, 16 Dec 2024 04:31:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ddffda77588312b8e9f475fea7ca744f53d6a1be2d9cbe31fdd40a29bd2d0`  
		Last Modified: Mon, 23 Dec 2024 04:26:36 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1d605ca856171d656bd54d5c8a440ecd263ab4520f3a1a45c1b49e90414813`  
		Last Modified: Mon, 06 Jan 2025 17:46:14 GMT  
		Size: 284.5 MB (284480629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fac8a15ea97e769dba45ff409bdb5a66011a55839ef22c97c520a93be06f0`  
		Last Modified: Mon, 23 Dec 2024 04:26:37 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Mon, 06 Jan 2025 22:46:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Mon, 16 Dec 2024 04:30:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Mon, 23 Dec 2024 04:25:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Last Modified: Tue, 07 Jan 2025 02:40:59 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Mon, 30 Dec 2024 04:21:31 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Mon, 16 Dec 2024 04:30:26 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
