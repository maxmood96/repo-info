## `julia:1-bookworm`

```console
$ docker pull julia@sha256:a33bd350c9565c1e63ce27f1039591df29203bb8579d103b1985ed93251af6f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:d9fb7721a706ff8409e12554841c081297099e18ac3e91649d85000a6b658a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323770493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd9c204a341ef6eeafd8e0eee6657b0927b19608bb44e3599aebfd3279d4ce0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:22:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:22:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:22:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:22:38 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 01:22:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:22:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88e149700235fd581c50b2dda1356cd66cb1fe0f296379f0989228162836bb`  
		Last Modified: Tue, 13 Jan 2026 01:23:32 GMT  
		Size: 5.7 MB (5717392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b66ef83e65da6516f986b87aa6f0282558aa34c1be62cd9d00b2726d14a4f6`  
		Last Modified: Tue, 13 Jan 2026 01:23:46 GMT  
		Size: 289.8 MB (289824163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7be4b0e690caf07cf7d5ae99f51bc0660a3fe3bb2863c007b6691b344d4a0`  
		Last Modified: Tue, 13 Jan 2026 01:23:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:044d221e4babdb24ae294e72d2e8685349064583064331dffc70e54b7405132a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45927c68f6817d13f16ee15d6843cbe71a9b255b33c0675ca73d1ba0c876f3b4`

```dockerfile
```

-	Layers:
	-	`sha256:24473821d74ab1486fb50a9a22d0de265c9c6717f86ca26518adfe618a960477`  
		Last Modified: Tue, 13 Jan 2026 01:23:20 GMT  
		Size: 2.6 MB (2567696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f990a0c64258c1fec5b81d354c545a782c4d7f8de93dbe05151e57088ce99f`  
		Last Modified: Tue, 13 Jan 2026 01:23:19 GMT  
		Size: 16.5 KB (16546 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7df69debe6e7b9d5e176ea0f91d5a65505b6aad70bdd076489b9ef28110157f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344948590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af62499fae014adde6c44706a1467725361fd60e68dfec7622d11f53572259b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:22:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:22:40 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:22:40 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:22:40 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:22:40 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 01:22:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:22:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:22:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6261cdbd0dfe0a5a37080c4e0d495c4f202ae5c0e908ac614c11ff7b79ea984`  
		Last Modified: Tue, 13 Jan 2026 01:23:27 GMT  
		Size: 5.6 MB (5567755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf441ca52a584796d6766b0f2a2eb115e6b1ed8222d81c9d970e8dd477f7952`  
		Last Modified: Tue, 13 Jan 2026 01:23:33 GMT  
		Size: 311.3 MB (311272579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f36a0f2f0d447c47d15f33bc6f7265affebeb061e1366e62b07fea0f36952e8`  
		Last Modified: Tue, 13 Jan 2026 01:23:41 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:151c56dcbd6f925baef578450639e99c8b234cb36bd9321a0da0f5e2022c11fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f40530ab143ebf523a1e6e1d02d7f4fc180161527f21034433c30675df5532`

```dockerfile
```

-	Layers:
	-	`sha256:12c9c237ad03513b98018ea102ee3ad801aaf529ed0fee46f53c1326973584f2`  
		Last Modified: Tue, 13 Jan 2026 01:23:27 GMT  
		Size: 2.6 MB (2567971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c68c44c61791e1147b79d21f11761ae3d46187ddfdec15c7ad9986465f19de5`  
		Last Modified: Tue, 13 Jan 2026 01:23:27 GMT  
		Size: 16.7 KB (16665 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:ff79315d3564940d86072e7ed90dc3d972c2bb9429ad72a30e68633b1d234164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266295707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1489ba87cf3b0b57c196abeb47a005e870cb5c0bb1388837429eaec10bf6c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Jan 2026 01:18:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Jan 2026 01:18:58 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 13 Jan 2026 01:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.4-linux-x86_64.tar.gz'; 			sha256='c57baf178fe140926acb1a25396d482f325af9d7908d9b066d2fbc0d6639985d'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.4-linux-i686.tar.gz'; 			sha256='fb7c91de825ecd6bc3d9960e9fc18c44052e82bcb4a5d2f626e6932de5f34968'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.4-linux-aarch64.tar.gz'; 			sha256='a602a2dfee931224fd68e47567dc672743e2fd9e80f39d84cf3c99afc9663ddd'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 13 Jan 2026 01:18:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Jan 2026 01:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:18:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226ce8b7e04a04fa6b26e2c2d91e45c34f22111596846479288481a9a0b17c1a`  
		Last Modified: Tue, 13 Jan 2026 01:19:29 GMT  
		Size: 5.9 MB (5878408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e5bc3d50ce9b90c97e946d51c176dde97ac5b648d6eafdd359c1c0f161f4e6`  
		Last Modified: Tue, 13 Jan 2026 01:19:34 GMT  
		Size: 231.2 MB (231206861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866423de7ae1c1430a3da51bcf61bf9525742d7839b4b4c884ef2735aeada9c4`  
		Last Modified: Tue, 13 Jan 2026 01:19:29 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0b861165d96eb671b80db24417b8ea94702868dba09b2a204842f37f03272417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a587441191ec347516d97030610b14943f4fff6ecf2bb8cac056c2986dd5bee`

```dockerfile
```

-	Layers:
	-	`sha256:c3484d6ab3102b2f72444ab78810bd8fdc50286bef8959851f668329952478f5`  
		Last Modified: Tue, 13 Jan 2026 01:19:29 GMT  
		Size: 2.6 MB (2564843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5388d9e5733901f1d4a328340e34074ece02d3b2924920ca756026970bd5e644`  
		Last Modified: Tue, 13 Jan 2026 03:04:45 GMT  
		Size: 16.5 KB (16513 bytes)  
		MIME: application/vnd.in-toto+json
