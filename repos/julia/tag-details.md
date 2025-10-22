<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-trixie`](#julia1-trixie)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1-windowsservercore-ltsc2025`](#julia1-windowsservercore-ltsc2025)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.21`](#julia110-alpine321)
-	[`julia:1.10-alpine3.22`](#julia110-alpine322)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-trixie`](#julia110-trixie)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10-windowsservercore-ltsc2025`](#julia110-windowsservercore-ltsc2025)
-	[`julia:1.10.10`](#julia11010)
-	[`julia:1.10.10-alpine`](#julia11010-alpine)
-	[`julia:1.10.10-alpine3.21`](#julia11010-alpine321)
-	[`julia:1.10.10-alpine3.22`](#julia11010-alpine322)
-	[`julia:1.10.10-bookworm`](#julia11010-bookworm)
-	[`julia:1.10.10-trixie`](#julia11010-trixie)
-	[`julia:1.10.10-windowsservercore`](#julia11010-windowsservercore)
-	[`julia:1.10.10-windowsservercore-ltsc2022`](#julia11010-windowsservercore-ltsc2022)
-	[`julia:1.10.10-windowsservercore-ltsc2025`](#julia11010-windowsservercore-ltsc2025)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-trixie`](#julia111-trixie)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11-windowsservercore-ltsc2025`](#julia111-windowsservercore-ltsc2025)
-	[`julia:1.11.7`](#julia1117)
-	[`julia:1.11.7-bookworm`](#julia1117-bookworm)
-	[`julia:1.11.7-trixie`](#julia1117-trixie)
-	[`julia:1.11.7-windowsservercore`](#julia1117-windowsservercore)
-	[`julia:1.11.7-windowsservercore-ltsc2022`](#julia1117-windowsservercore-ltsc2022)
-	[`julia:1.11.7-windowsservercore-ltsc2025`](#julia1117-windowsservercore-ltsc2025)
-	[`julia:1.12`](#julia112)
-	[`julia:1.12-bookworm`](#julia112-bookworm)
-	[`julia:1.12-trixie`](#julia112-trixie)
-	[`julia:1.12-windowsservercore`](#julia112-windowsservercore)
-	[`julia:1.12-windowsservercore-ltsc2022`](#julia112-windowsservercore-ltsc2022)
-	[`julia:1.12-windowsservercore-ltsc2025`](#julia112-windowsservercore-ltsc2025)
-	[`julia:1.12.1`](#julia1121)
-	[`julia:1.12.1-bookworm`](#julia1121-bookworm)
-	[`julia:1.12.1-trixie`](#julia1121-trixie)
-	[`julia:1.12.1-windowsservercore`](#julia1121-windowsservercore)
-	[`julia:1.12.1-windowsservercore-ltsc2022`](#julia1121-windowsservercore-ltsc2022)
-	[`julia:1.12.1-windowsservercore-ltsc2025`](#julia1121-windowsservercore-ltsc2025)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:latest`](#julialatest)
-	[`julia:trixie`](#juliatrixie)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)
-	[`julia:windowsservercore-ltsc2025`](#juliawindowsservercore-ltsc2025)

## `julia:1`

```console
$ docker pull julia@sha256:6df3a44f17932272ac3524a39c554bf942a49902da0ed8f58f70beb03cf0b691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:f769ef90b49807694da53abb2ca8c6c67532b9e64d7b7bb5571f76d5ff477fcf
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
$ docker pull julia@sha256:1aa85df6ec49583176b3d63173ff7a2c4e9331ae0b9f972855300f7c42f87ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df569a38312c003e97032a8400079825dee34a9312690f12cac8da07192240cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230bd169a62bdd742f5fe1526024758c9182734b2090afb36f7e9b11e1d56c1f`  
		Last Modified: Tue, 21 Oct 2025 20:15:41 GMT  
		Size: 5.7 MB (5716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b94ddc353e5019807ab431f31f99fde76c06428fd4cf7e028e597d04a5740`  
		Last Modified: Wed, 22 Oct 2025 01:18:52 GMT  
		Size: 289.5 MB (289470982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f404cac60bf373235bd1c33e9eeb8a524d328181898fbcffc99312339216d02`  
		Last Modified: Tue, 21 Oct 2025 20:15:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c44d1a92f620cbf4341c7925e7df60c230efd111d753fd591bfd8ec514038e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e1512307c7da2bd465c639735be18e024d648fa0b91349b19b9d380be9df86`

```dockerfile
```

-	Layers:
	-	`sha256:584b20012bf0215b3e38226088d4e60467593cb18f440178131d34325a173ce7`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f32c356b06f4210b222c36b6e0d30b546d1eb64c6ac6bd3881a552b91de57ec`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:db7e63bcfaec71ea6e4281b4e92d081a1764b56cc6a9ff17cc15962b840cbd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcebdb683edeca155ae87ab12b238118291e7afeef30cd4d65bbb47dc57b98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5291731e8c0d3673a1a88ec62c3b52a25f60c6b223611669ff46969390581`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 5.6 MB (5567174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9c6938264fafd3aec09c37207ec05ed10474b77334515ecc4ec31d88bf5e1`  
		Last Modified: Tue, 21 Oct 2025 22:31:49 GMT  
		Size: 310.2 MB (310205330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974b20ce9e4f47cf1dc904cdd42abc7dd5ce1273805b63d020904d9e5676047`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:080e22faa91f324fdc0b3bcab563ac06d536a855ad787d9507c6a08a2b6fbfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdc62b09c5f7605ac15c3b7dbe4873246cfb7b61cb2406bc84e816b58de00c5`

```dockerfile
```

-	Layers:
	-	`sha256:12f1b6fb81092bc32c3ec2e038592a894653eefde55b19513b91d9b1cd84b882`  
		Last Modified: Tue, 21 Oct 2025 20:02:36 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a91fb3011ec1aeadac1477bea3e37c91e22e3dec83e151e44348b9c88428366`  
		Last Modified: Tue, 21 Oct 2025 20:02:37 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d5f8bf506eac97acd36cb2b8f406a27119d33b7f4dd0f25fd5ba83e45f67cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dcff817f5a853949791b9226becba3a5c8264b8251fcc8c8a347ae0ecb3c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac3a9ad9b8eabd3b5d50f72eebebfa697cdbb06c950c34087e6289736881bb0`  
		Last Modified: Tue, 21 Oct 2025 18:17:26 GMT  
		Size: 5.9 MB (5878048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04cdd9874dc106b265e5ba8b55d1e1d1c26603f7682c64f4365b76322b55d54`  
		Last Modified: Tue, 21 Oct 2025 22:31:16 GMT  
		Size: 231.0 MB (231003075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55c53a4a537b4baf40d7dd1a9782baf04a5bcd8647966a03bb1bbcabadb072`  
		Last Modified: Tue, 21 Oct 2025 18:17:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c34b15651101f3a14a8601b87b38e9dee4442fb327c129b770ac5fb1e5b1381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1b43567d7d2e8ebbaf9036174313b13740f20b7df0f50acbf80d2e87bcdb5d`

```dockerfile
```

-	Layers:
	-	`sha256:cddd1c3c366ee6a4f085600d7a1893078914ecdb31df262b989de8065683e47a`  
		Last Modified: Tue, 21 Oct 2025 20:02:41 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba22b294c989c47dcd755204201d14d2141f0e24bba2f0b2f23e9e827d7a59c0`  
		Last Modified: Tue, 21 Oct 2025 20:02:42 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-trixie`

```console
$ docker pull julia@sha256:0d11d89a94c97c35ba7f1acc8e77287b47dbd69a24e078b210d11c21f69ea7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:dde8fbb99f3a8cc20ff9248560e471f28794406993756d349d0ca67839562ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:da76ee4b1c8838bf073c4463082881c9edbed92a046d4d9f3ec7a3785fbd37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3f33be8fe9e3496a9e954d3af5f3466caf3201d9c8c009df451489829551d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:a15118be592efefffd3eb87af0e1af3d573f1014b2fd6334a24693389569db22
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
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:171e8a5fc64c8acf452dc5eb8e35867048f7b52e396bd2f8d9bb32879dfb78ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c0dc3eeeb6d983dfd6b11756d830ec08a7e15a67f4df66b55c48fb2121da6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b6514be2fdb4df0784d0c6d265b9736a3fda7dc8d3278c5fadc3f460411b6e`  
		Last Modified: Tue, 21 Oct 2025 01:29:39 GMT  
		Size: 6.2 MB (6242721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8376bab843477c63f1a903e9052f5423c1f32ad5281d38f365b21283194328`  
		Last Modified: Tue, 21 Oct 2025 11:18:47 GMT  
		Size: 176.4 MB (176362186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312a0b56be934b80a01b6e9b5df17eae9ad346528db3259e0038063290e27e9`  
		Last Modified: Tue, 21 Oct 2025 01:29:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:e6249fd9e30017ec06d8dd6d0ef078272e8590671d2e9cd9d8ca784d0d71ba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34252a4fad6d01efee29409a60454f1b7aee539b6c4552495094cffa4686d0f6`

```dockerfile
```

-	Layers:
	-	`sha256:f685c3ef5f9352c3b371bdb93706b3d6f6d280753caf841f4e069e1985a6590f`  
		Last Modified: Tue, 21 Oct 2025 11:02:40 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4e605a73c3f29f0f7d53882a0e566bb0e3a86955889a4e14ad74d1cf10bed6`  
		Last Modified: Tue, 21 Oct 2025 11:02:42 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0239f692dba1d0d42c19d420ec672a7b3601db65eab9920cdcfba5bf48fc0b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213745597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc5428e2fd7f01fd8e5ee155bd30a40152186bfb01a317e4a2fa5a2d813bf88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38525cd6f78da9fe5917c1c21169e062879af73a6472e7ac9963d8f2b1463f7`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6153026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a6c2ef61011ed5ba1789ce07901841387015b024de528eeaaf76847b08137`  
		Last Modified: Tue, 21 Oct 2025 09:59:26 GMT  
		Size: 177.5 MB (177450078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9f69a7f3d5115598c06e2d346fe6be0774b3bd22f47727a24a51354b8563b`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:b4a936149a26a183114c94639fddc55d39ff48461c48565e880b87e3f09a8172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927cad95cf4f15f1f52a85791a409dc0f4ad0c6aeacfbfcec497d42459d60c5f`

```dockerfile
```

-	Layers:
	-	`sha256:c19d85ca0548f0d6cc587c82286ca6693f42d10b632606d173ee6cba564965b5`  
		Last Modified: Tue, 21 Oct 2025 08:02:22 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2971538095a08b1b1da12832e3c5f1958d99ef1da1e4ea3d1e8b4f837f2a91`  
		Last Modified: Tue, 21 Oct 2025 08:02:23 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:0705758aeb67f7bc90ad7a7bb8179e31aac2a3f0bde668724f4174a77b4aab38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c3565aaac74483ba08f8641f67ec87282809e1490714b7fc50a5b5cec8fcc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f966b3cc15e4cb49ec9bb8df24e0c88bf15746ebae8548e96fbbb93633d5a0`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a8e7fa3869efc4a509f98572ab506e421276af500708f787443aeb4400def`  
		Last Modified: Tue, 21 Oct 2025 01:19:05 GMT  
		Size: 157.8 MB (157841879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662b7f81de827a3380f5546b30129577c4fcaf02c72239deaa89310944f066e`  
		Last Modified: Tue, 21 Oct 2025 01:19:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:2391cd75f75437374cbddad89f0aab02de737b669a4ebe28a23ee2f9710b0b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b755542b72a9aa98ad7d3ae120b8300ea1003802d0de7a58d42a814267f72a57`

```dockerfile
```

-	Layers:
	-	`sha256:76ff8ca1e4dc815578aad8ddca8aaa4626192cb6eb1d5fa0df79c4002f4dd6e6`  
		Last Modified: Tue, 21 Oct 2025 11:02:48 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a1c40a1578f4d68aafdd9c1a4d827a59508836bbfc310e97d1c57fbd7554fd`  
		Last Modified: Tue, 21 Oct 2025 11:02:49 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:4042a0d68db8686e48335f06fcc6cdceb2fe96d045c847c4461513df0a0f261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44f202b74bfeffe7433cb8c2a25e796e490a54062a438c29cb9c6ea313bb74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da13a7f27803c776568aca71a6cabc5ddf5ed82c2f7cc0348cd05e52debf21`  
		Last Modified: Tue, 21 Oct 2025 03:58:38 GMT  
		Size: 155.4 MB (155388365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c84e2e6978ed83fb08cd18bed60c508f9de0b5ef024d15b3c434d21a14364f`  
		Last Modified: Tue, 21 Oct 2025 02:02:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:16d7d83e82171e92042a8795fdb8148f328b7e08f36c96621362d47e3b3f6229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab92b9c43318187ad5dd7ffb7b1d71fe446bd86ab76cea2a750fa3b54b70c393`

```dockerfile
```

-	Layers:
	-	`sha256:62cecf066859dea5b0321d01b076a4fae44ae56c8849a76033ed07391898f966`  
		Last Modified: Tue, 21 Oct 2025 05:02:30 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5830d2c56244f939e74422344e6958eb6f885bfb31f1ad7919bcd39fd14ff56e`  
		Last Modified: Tue, 21 Oct 2025 05:02:31 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:f3c97d1e2d7fb192166f1dfa792a121d59a247380a8984016ff1bb3a2b110743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409264907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8aed3f999fce7f0dc4ceeecb0c032760cb299b77698d9f674f7e5a09c57e14`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:43:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:44:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c51f38aa013c2055a61a5f4a1d2349666eb9457e574fe677c96bbd46b9e55c`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe1604df2b99eba86d1d80ece03ad84ea7917e7b33cdb0a9b84f01b3347255`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72b26b1d61f16966ff8b108660abe3e3ab028e7d36a5c65aaed346bdbea6b8`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa9b25d3173de6f519caeb4758cd9ff20b540b49cd40f5f366e05f6c37d472b`  
		Last Modified: Tue, 14 Oct 2025 21:36:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b3b144bcb26e0de9b8c8a5e7bc278cbed04696d69a361e6a1344302aa957f`  
		Last Modified: Tue, 14 Oct 2025 23:03:11 GMT  
		Size: 188.8 MB (188777893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf54f68dc216b1db2632a56ce7266059422ed1c29e8b8beb236ba9ff78977ce`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:468da5ad969609da851733e9c20b4fdbebea12f1386f1c8175c60f364133ac8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1677810088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e08269a98333beb3e137791613a7adb2ea0c4cf0c67a9c0e1eab434a3972a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:43:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5601680face9cd24ed8439d5d819578a5a6e960e1c1890e9c1038facd81b9ee`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb5079dc730813a1d1f566cd6f3636b3d1959c605a6340200181dd8d2c546ac`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653aa7f3d49f56c710d8b384f0aaaadfc59990fdee5a76d0ffd7cec6cfc3d10e`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedccef22ecdcd576e671f208da349b7493e2a1ddcb624a5aadf2c6ce3b436b`  
		Last Modified: Tue, 14 Oct 2025 23:03:07 GMT  
		Size: 188.8 MB (188784436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acedfad45cac3565fdd41240e3bd0e4163609c9828507bcc0e6e134330c427a`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:d1a3e070ace2a47e5eb3cf2e507a090c9b0be78e986d61fa40b7b708e53a3842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:52ac97bc4b7d2863b731985c6614a46e6ab4f13f13f3c8d91d933a5c13055102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181941938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df008c40538a112568d8ff3054242fbabee9d18edd7f08445c7c38cf6f7cea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bda53ebb21b1322cf919f16ba5b28ae9b1d9acd8c0d0da1518623793417c9`  
		Last Modified: Sat, 11 Oct 2025 01:40:30 GMT  
		Size: 178.3 MB (178298998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d772ec346b861be7ae3ae4939fab2ea82732b66bf0931f5d9a7cb217646c0c6`  
		Last Modified: Wed, 08 Oct 2025 23:29:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:9b1b7279a096a1493387b3ed071e6f6201a78ed8dfd3ecc09596e34b48a8e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a9169be517a413e716324eb64afaf1e70b5e4bf29b7ab8205696d41c42cfd`

```dockerfile
```

-	Layers:
	-	`sha256:d87cc8698e0b72551245a2ae783ddb2d064e0bf0c6a2b90e877668ed5777c209`  
		Last Modified: Thu, 09 Oct 2025 02:02:25 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b3221cfc383c0844d2d950de60a17caa749b9d059d4a7e43848dc1f00be791`  
		Last Modified: Thu, 09 Oct 2025 02:02:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.22`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:71bf8dd5cea601085b5e5bda831ee0ca94cc7c2976fde387c58864630778c1cb
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
$ docker pull julia@sha256:56ca89a4913111a3df25b7cdc4bc77642f1a1ded3ac43660c2e66a8eefb20c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb98ec8b77011c7171bae247431a414460552e065967960acab8af8463399cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadaf0b1f5567f40dc2814fa5f45c5fa2670bf6c720e01f1b1bdb517f583d8c1`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 5.7 MB (5716321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e569c877561a6133f73a70ff560f923963fcfc6b02b65c269cabecfed2501da3`  
		Last Modified: Tue, 21 Oct 2025 11:05:06 GMT  
		Size: 176.3 MB (176324295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b022015f0b8155f53e40bf620a31cd1ad80f016826d9c7ef62350e5efa614`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0c263d68101b28aa6c405c25ecd175293e6f2c46a1185d5feb539d4396b950b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0415041bed2d86f2fce6a6b1980599168066c0bbc2ea5c1d322b956ee22b578b`

```dockerfile
```

-	Layers:
	-	`sha256:f7f573e8cc8a009e9c62e2bd525e60fff99fbbc8b820473bab70070bfbbb11f9`  
		Last Modified: Tue, 21 Oct 2025 11:02:49 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2d2dcc3b86e47ba5a4bec6ccd72ff86d3d6e2353e61b52c4190a4e0bb54960`  
		Last Modified: Tue, 21 Oct 2025 11:02:50 GMT  
		Size: 16.6 KB (16641 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c3130bbdfb0559135e7e4fd3ec3ce444ad642a3caa27fb0305ead377a5ba1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211081933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7e3d3935b40dfd41e295b20c7ab986fd313a3b2dee197f9254afcda97996bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7930cebf84a215d9eb527b9278102385789e575096e6a1a5decc8dc34c5c007f`  
		Last Modified: Tue, 21 Oct 2025 01:20:23 GMT  
		Size: 5.6 MB (5567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416814b75386b08ccd9efc878f5b1bc15709a2a71fc3ffebd1a092d755e9f1d3`  
		Last Modified: Wed, 22 Oct 2025 12:39:10 GMT  
		Size: 177.4 MB (177412306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89f0b4eeb4bf4a2193878aceff84d44746dccf95da007ea8629584b3a9b027`  
		Last Modified: Tue, 21 Oct 2025 01:21:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a6b95972daf4e0e6df5ce08df964d84009b03bde5ba141c8a45acf6969ecd8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd6d40a3535c364489348457caf353b2c83f97b5cc3beae4e369728b71ea11b`

```dockerfile
```

-	Layers:
	-	`sha256:0e9c1065e40271bc546b2304d9b2243d96d16a0da5ebf5231b5e335ae02cc761`  
		Last Modified: Tue, 21 Oct 2025 08:02:29 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3355becbc13b4ce3459da9b6c637c6d87c240b5733b9001efe32a4756681cc`  
		Last Modified: Tue, 21 Oct 2025 08:02:30 GMT  
		Size: 16.7 KB (16735 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:179ebe72059e625727a4736be24707996f49692aecc554661434ddb340887238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192895973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855ca2f4f13088b54f82af4e38f806fb3c1d764e3afbf57540d1fc3e561afae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ab4918e431ea323c9daec4dafe9801c0dd4b05fcfd38b1b494a2ba0b322325`  
		Last Modified: Tue, 21 Oct 2025 01:19:29 GMT  
		Size: 5.9 MB (5878032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cffbc8da390394fd981f2bd70983ba3930f30f9bcf7fb3e2b2f015829fc812a`  
		Last Modified: Tue, 21 Oct 2025 01:19:21 GMT  
		Size: 157.8 MB (157807895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69545198becd2e773efc013832bbf758d85363e6493e2cd377e0e148664e806d`  
		Last Modified: Tue, 21 Oct 2025 01:19:28 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8b88744c754dc4bb32d6c0826aa999a64d05129cbe02424cf799ed5ec2696df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a892247c2c5f8fac45878c6db509c9d11dcf18e1ccdbd51da473db035cd2f0`

```dockerfile
```

-	Layers:
	-	`sha256:1a9a6f23d48d24ef5021b38a903e06500289bec5d1f666ac4166e7bfaa9c5859`  
		Last Modified: Tue, 21 Oct 2025 11:02:56 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d25c997bf28e7be184be14f9e2940b8e9d9c32220ab6845f810fe4f7d8f647`  
		Last Modified: Tue, 21 Oct 2025 11:02:57 GMT  
		Size: 16.6 KB (16617 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:82ae3c194c2009ca9f2a8edadc20a231612fefa360b5f7be0cca2cb8ad8cc32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f03ee3ded076f2fdbe02b9bc806a7f5a7f0557774745d081a7ce044661e0db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc155374c7db12d97ec8dfc57f566dd402662f9a5876305b298bced2fb30309b`  
		Last Modified: Tue, 21 Oct 2025 01:46:55 GMT  
		Size: 6.3 MB (6256276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da959eb093540b25d0974705d27b2eaa0cf9bb54738f3bfb11b917259e8b9d1`  
		Last Modified: Tue, 21 Oct 2025 01:50:42 GMT  
		Size: 155.4 MB (155354835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fce20b9476a27fed9f408abf77260dba6eb85cb99d1c7499f41f28e59df296`  
		Last Modified: Tue, 21 Oct 2025 01:50:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0751301f06b4a89e7a7a7ba740c617e1e99d0062078016608867ea197e876cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6084b56427bb65bc0f5e8cf66115b42d6b33773b8829a3387f7052450c48ced`

```dockerfile
```

-	Layers:
	-	`sha256:ff6bdc2ae85d9e0d9900bf628e28fc7ae8a6b063fad4e15def017dfa29ce7a63`  
		Last Modified: Tue, 21 Oct 2025 05:02:36 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbd4e35b3f2cbb7994174ca2d996f998336c04399b864fac7c5af1d42e33372`  
		Last Modified: Tue, 21 Oct 2025 05:02:37 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-trixie`

```console
$ docker pull julia@sha256:e775b60db76f95d737365d8964a2bf5e66e8187e6fd6bc631f318dc6fe4a7974
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

### `julia:1.10-trixie` - linux; amd64

```console
$ docker pull julia@sha256:171e8a5fc64c8acf452dc5eb8e35867048f7b52e396bd2f8d9bb32879dfb78ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c0dc3eeeb6d983dfd6b11756d830ec08a7e15a67f4df66b55c48fb2121da6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b6514be2fdb4df0784d0c6d265b9736a3fda7dc8d3278c5fadc3f460411b6e`  
		Last Modified: Tue, 21 Oct 2025 01:29:39 GMT  
		Size: 6.2 MB (6242721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8376bab843477c63f1a903e9052f5423c1f32ad5281d38f365b21283194328`  
		Last Modified: Tue, 21 Oct 2025 11:18:47 GMT  
		Size: 176.4 MB (176362186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312a0b56be934b80a01b6e9b5df17eae9ad346528db3259e0038063290e27e9`  
		Last Modified: Tue, 21 Oct 2025 01:29:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:e6249fd9e30017ec06d8dd6d0ef078272e8590671d2e9cd9d8ca784d0d71ba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34252a4fad6d01efee29409a60454f1b7aee539b6c4552495094cffa4686d0f6`

```dockerfile
```

-	Layers:
	-	`sha256:f685c3ef5f9352c3b371bdb93706b3d6f6d280753caf841f4e069e1985a6590f`  
		Last Modified: Tue, 21 Oct 2025 11:02:40 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4e605a73c3f29f0f7d53882a0e566bb0e3a86955889a4e14ad74d1cf10bed6`  
		Last Modified: Tue, 21 Oct 2025 11:02:42 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0239f692dba1d0d42c19d420ec672a7b3601db65eab9920cdcfba5bf48fc0b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213745597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc5428e2fd7f01fd8e5ee155bd30a40152186bfb01a317e4a2fa5a2d813bf88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38525cd6f78da9fe5917c1c21169e062879af73a6472e7ac9963d8f2b1463f7`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6153026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a6c2ef61011ed5ba1789ce07901841387015b024de528eeaaf76847b08137`  
		Last Modified: Tue, 21 Oct 2025 09:59:26 GMT  
		Size: 177.5 MB (177450078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9f69a7f3d5115598c06e2d346fe6be0774b3bd22f47727a24a51354b8563b`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b4a936149a26a183114c94639fddc55d39ff48461c48565e880b87e3f09a8172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927cad95cf4f15f1f52a85791a409dc0f4ad0c6aeacfbfcec497d42459d60c5f`

```dockerfile
```

-	Layers:
	-	`sha256:c19d85ca0548f0d6cc587c82286ca6693f42d10b632606d173ee6cba564965b5`  
		Last Modified: Tue, 21 Oct 2025 08:02:22 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2971538095a08b1b1da12832e3c5f1958d99ef1da1e4ea3d1e8b4f837f2a91`  
		Last Modified: Tue, 21 Oct 2025 08:02:23 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:0705758aeb67f7bc90ad7a7bb8179e31aac2a3f0bde668724f4174a77b4aab38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c3565aaac74483ba08f8641f67ec87282809e1490714b7fc50a5b5cec8fcc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f966b3cc15e4cb49ec9bb8df24e0c88bf15746ebae8548e96fbbb93633d5a0`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a8e7fa3869efc4a509f98572ab506e421276af500708f787443aeb4400def`  
		Last Modified: Tue, 21 Oct 2025 01:19:05 GMT  
		Size: 157.8 MB (157841879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662b7f81de827a3380f5546b30129577c4fcaf02c72239deaa89310944f066e`  
		Last Modified: Tue, 21 Oct 2025 01:19:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2391cd75f75437374cbddad89f0aab02de737b669a4ebe28a23ee2f9710b0b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b755542b72a9aa98ad7d3ae120b8300ea1003802d0de7a58d42a814267f72a57`

```dockerfile
```

-	Layers:
	-	`sha256:76ff8ca1e4dc815578aad8ddca8aaa4626192cb6eb1d5fa0df79c4002f4dd6e6`  
		Last Modified: Tue, 21 Oct 2025 11:02:48 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a1c40a1578f4d68aafdd9c1a4d827a59508836bbfc310e97d1c57fbd7554fd`  
		Last Modified: Tue, 21 Oct 2025 11:02:49 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:4042a0d68db8686e48335f06fcc6cdceb2fe96d045c847c4461513df0a0f261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44f202b74bfeffe7433cb8c2a25e796e490a54062a438c29cb9c6ea313bb74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da13a7f27803c776568aca71a6cabc5ddf5ed82c2f7cc0348cd05e52debf21`  
		Last Modified: Tue, 21 Oct 2025 03:58:38 GMT  
		Size: 155.4 MB (155388365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c84e2e6978ed83fb08cd18bed60c508f9de0b5ef024d15b3c434d21a14364f`  
		Last Modified: Tue, 21 Oct 2025 02:02:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:16d7d83e82171e92042a8795fdb8148f328b7e08f36c96621362d47e3b3f6229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab92b9c43318187ad5dd7ffb7b1d71fe446bd86ab76cea2a750fa3b54b70c393`

```dockerfile
```

-	Layers:
	-	`sha256:62cecf066859dea5b0321d01b076a4fae44ae56c8849a76033ed07391898f966`  
		Last Modified: Tue, 21 Oct 2025 05:02:30 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5830d2c56244f939e74422344e6958eb6f885bfb31f1ad7919bcd39fd14ff56e`  
		Last Modified: Tue, 21 Oct 2025 05:02:31 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:3de3c91fc7e43489691d08752394eb872add49cabf2362dc48d91b86051dfed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:f3c97d1e2d7fb192166f1dfa792a121d59a247380a8984016ff1bb3a2b110743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409264907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8aed3f999fce7f0dc4ceeecb0c032760cb299b77698d9f674f7e5a09c57e14`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:43:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:44:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c51f38aa013c2055a61a5f4a1d2349666eb9457e574fe677c96bbd46b9e55c`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe1604df2b99eba86d1d80ece03ad84ea7917e7b33cdb0a9b84f01b3347255`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72b26b1d61f16966ff8b108660abe3e3ab028e7d36a5c65aaed346bdbea6b8`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa9b25d3173de6f519caeb4758cd9ff20b540b49cd40f5f366e05f6c37d472b`  
		Last Modified: Tue, 14 Oct 2025 21:36:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b3b144bcb26e0de9b8c8a5e7bc278cbed04696d69a361e6a1344302aa957f`  
		Last Modified: Tue, 14 Oct 2025 23:03:11 GMT  
		Size: 188.8 MB (188777893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf54f68dc216b1db2632a56ce7266059422ed1c29e8b8beb236ba9ff78977ce`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:468da5ad969609da851733e9c20b4fdbebea12f1386f1c8175c60f364133ac8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1677810088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e08269a98333beb3e137791613a7adb2ea0c4cf0c67a9c0e1eab434a3972a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:43:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5601680face9cd24ed8439d5d819578a5a6e960e1c1890e9c1038facd81b9ee`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb5079dc730813a1d1f566cd6f3636b3d1959c605a6340200181dd8d2c546ac`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653aa7f3d49f56c710d8b384f0aaaadfc59990fdee5a76d0ffd7cec6cfc3d10e`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedccef22ecdcd576e671f208da349b7493e2a1ddcb624a5aadf2c6ce3b436b`  
		Last Modified: Tue, 14 Oct 2025 23:03:07 GMT  
		Size: 188.8 MB (188784436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acedfad45cac3565fdd41240e3bd0e4163609c9828507bcc0e6e134330c427a`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6a4c454e6a05b7c84ff96eff12eae0db007d22e2fba00b72ddf48222b5ea0bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:468da5ad969609da851733e9c20b4fdbebea12f1386f1c8175c60f364133ac8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1677810088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e08269a98333beb3e137791613a7adb2ea0c4cf0c67a9c0e1eab434a3972a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:43:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5601680face9cd24ed8439d5d819578a5a6e960e1c1890e9c1038facd81b9ee`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb5079dc730813a1d1f566cd6f3636b3d1959c605a6340200181dd8d2c546ac`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653aa7f3d49f56c710d8b384f0aaaadfc59990fdee5a76d0ffd7cec6cfc3d10e`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedccef22ecdcd576e671f208da349b7493e2a1ddcb624a5aadf2c6ce3b436b`  
		Last Modified: Tue, 14 Oct 2025 23:03:07 GMT  
		Size: 188.8 MB (188784436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acedfad45cac3565fdd41240e3bd0e4163609c9828507bcc0e6e134330c427a`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:1e3df351c3942a018cb4879d6c45d76830c9ca55e1ba5f737932eb92fed1dfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:f3c97d1e2d7fb192166f1dfa792a121d59a247380a8984016ff1bb3a2b110743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409264907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8aed3f999fce7f0dc4ceeecb0c032760cb299b77698d9f674f7e5a09c57e14`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:43:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:44:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c51f38aa013c2055a61a5f4a1d2349666eb9457e574fe677c96bbd46b9e55c`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe1604df2b99eba86d1d80ece03ad84ea7917e7b33cdb0a9b84f01b3347255`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72b26b1d61f16966ff8b108660abe3e3ab028e7d36a5c65aaed346bdbea6b8`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa9b25d3173de6f519caeb4758cd9ff20b540b49cd40f5f366e05f6c37d472b`  
		Last Modified: Tue, 14 Oct 2025 21:36:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b3b144bcb26e0de9b8c8a5e7bc278cbed04696d69a361e6a1344302aa957f`  
		Last Modified: Tue, 14 Oct 2025 23:03:11 GMT  
		Size: 188.8 MB (188777893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf54f68dc216b1db2632a56ce7266059422ed1c29e8b8beb236ba9ff78977ce`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10`

```console
$ docker pull julia@sha256:a15118be592efefffd3eb87af0e1af3d573f1014b2fd6334a24693389569db22
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
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.10.10` - linux; amd64

```console
$ docker pull julia@sha256:171e8a5fc64c8acf452dc5eb8e35867048f7b52e396bd2f8d9bb32879dfb78ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c0dc3eeeb6d983dfd6b11756d830ec08a7e15a67f4df66b55c48fb2121da6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b6514be2fdb4df0784d0c6d265b9736a3fda7dc8d3278c5fadc3f460411b6e`  
		Last Modified: Tue, 21 Oct 2025 01:29:39 GMT  
		Size: 6.2 MB (6242721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8376bab843477c63f1a903e9052f5423c1f32ad5281d38f365b21283194328`  
		Last Modified: Tue, 21 Oct 2025 11:18:47 GMT  
		Size: 176.4 MB (176362186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312a0b56be934b80a01b6e9b5df17eae9ad346528db3259e0038063290e27e9`  
		Last Modified: Tue, 21 Oct 2025 01:29:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:e6249fd9e30017ec06d8dd6d0ef078272e8590671d2e9cd9d8ca784d0d71ba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34252a4fad6d01efee29409a60454f1b7aee539b6c4552495094cffa4686d0f6`

```dockerfile
```

-	Layers:
	-	`sha256:f685c3ef5f9352c3b371bdb93706b3d6f6d280753caf841f4e069e1985a6590f`  
		Last Modified: Tue, 21 Oct 2025 11:02:40 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4e605a73c3f29f0f7d53882a0e566bb0e3a86955889a4e14ad74d1cf10bed6`  
		Last Modified: Tue, 21 Oct 2025 11:02:42 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0239f692dba1d0d42c19d420ec672a7b3601db65eab9920cdcfba5bf48fc0b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213745597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc5428e2fd7f01fd8e5ee155bd30a40152186bfb01a317e4a2fa5a2d813bf88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38525cd6f78da9fe5917c1c21169e062879af73a6472e7ac9963d8f2b1463f7`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6153026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a6c2ef61011ed5ba1789ce07901841387015b024de528eeaaf76847b08137`  
		Last Modified: Tue, 21 Oct 2025 09:59:26 GMT  
		Size: 177.5 MB (177450078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9f69a7f3d5115598c06e2d346fe6be0774b3bd22f47727a24a51354b8563b`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:b4a936149a26a183114c94639fddc55d39ff48461c48565e880b87e3f09a8172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927cad95cf4f15f1f52a85791a409dc0f4ad0c6aeacfbfcec497d42459d60c5f`

```dockerfile
```

-	Layers:
	-	`sha256:c19d85ca0548f0d6cc587c82286ca6693f42d10b632606d173ee6cba564965b5`  
		Last Modified: Tue, 21 Oct 2025 08:02:22 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2971538095a08b1b1da12832e3c5f1958d99ef1da1e4ea3d1e8b4f837f2a91`  
		Last Modified: Tue, 21 Oct 2025 08:02:23 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; 386

```console
$ docker pull julia@sha256:0705758aeb67f7bc90ad7a7bb8179e31aac2a3f0bde668724f4174a77b4aab38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c3565aaac74483ba08f8641f67ec87282809e1490714b7fc50a5b5cec8fcc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f966b3cc15e4cb49ec9bb8df24e0c88bf15746ebae8548e96fbbb93633d5a0`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a8e7fa3869efc4a509f98572ab506e421276af500708f787443aeb4400def`  
		Last Modified: Tue, 21 Oct 2025 01:19:05 GMT  
		Size: 157.8 MB (157841879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662b7f81de827a3380f5546b30129577c4fcaf02c72239deaa89310944f066e`  
		Last Modified: Tue, 21 Oct 2025 01:19:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:2391cd75f75437374cbddad89f0aab02de737b669a4ebe28a23ee2f9710b0b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b755542b72a9aa98ad7d3ae120b8300ea1003802d0de7a58d42a814267f72a57`

```dockerfile
```

-	Layers:
	-	`sha256:76ff8ca1e4dc815578aad8ddca8aaa4626192cb6eb1d5fa0df79c4002f4dd6e6`  
		Last Modified: Tue, 21 Oct 2025 11:02:48 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a1c40a1578f4d68aafdd9c1a4d827a59508836bbfc310e97d1c57fbd7554fd`  
		Last Modified: Tue, 21 Oct 2025 11:02:49 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; ppc64le

```console
$ docker pull julia@sha256:4042a0d68db8686e48335f06fcc6cdceb2fe96d045c847c4461513df0a0f261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44f202b74bfeffe7433cb8c2a25e796e490a54062a438c29cb9c6ea313bb74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da13a7f27803c776568aca71a6cabc5ddf5ed82c2f7cc0348cd05e52debf21`  
		Last Modified: Tue, 21 Oct 2025 03:58:38 GMT  
		Size: 155.4 MB (155388365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c84e2e6978ed83fb08cd18bed60c508f9de0b5ef024d15b3c434d21a14364f`  
		Last Modified: Tue, 21 Oct 2025 02:02:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:16d7d83e82171e92042a8795fdb8148f328b7e08f36c96621362d47e3b3f6229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab92b9c43318187ad5dd7ffb7b1d71fe446bd86ab76cea2a750fa3b54b70c393`

```dockerfile
```

-	Layers:
	-	`sha256:62cecf066859dea5b0321d01b076a4fae44ae56c8849a76033ed07391898f966`  
		Last Modified: Tue, 21 Oct 2025 05:02:30 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5830d2c56244f939e74422344e6958eb6f885bfb31f1ad7919bcd39fd14ff56e`  
		Last Modified: Tue, 21 Oct 2025 05:02:31 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:f3c97d1e2d7fb192166f1dfa792a121d59a247380a8984016ff1bb3a2b110743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409264907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8aed3f999fce7f0dc4ceeecb0c032760cb299b77698d9f674f7e5a09c57e14`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:43:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:44:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c51f38aa013c2055a61a5f4a1d2349666eb9457e574fe677c96bbd46b9e55c`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe1604df2b99eba86d1d80ece03ad84ea7917e7b33cdb0a9b84f01b3347255`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72b26b1d61f16966ff8b108660abe3e3ab028e7d36a5c65aaed346bdbea6b8`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa9b25d3173de6f519caeb4758cd9ff20b540b49cd40f5f366e05f6c37d472b`  
		Last Modified: Tue, 14 Oct 2025 21:36:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b3b144bcb26e0de9b8c8a5e7bc278cbed04696d69a361e6a1344302aa957f`  
		Last Modified: Tue, 14 Oct 2025 23:03:11 GMT  
		Size: 188.8 MB (188777893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf54f68dc216b1db2632a56ce7266059422ed1c29e8b8beb236ba9ff78977ce`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:468da5ad969609da851733e9c20b4fdbebea12f1386f1c8175c60f364133ac8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1677810088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e08269a98333beb3e137791613a7adb2ea0c4cf0c67a9c0e1eab434a3972a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:43:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5601680face9cd24ed8439d5d819578a5a6e960e1c1890e9c1038facd81b9ee`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb5079dc730813a1d1f566cd6f3636b3d1959c605a6340200181dd8d2c546ac`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653aa7f3d49f56c710d8b384f0aaaadfc59990fdee5a76d0ffd7cec6cfc3d10e`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedccef22ecdcd576e671f208da349b7493e2a1ddcb624a5aadf2c6ce3b436b`  
		Last Modified: Tue, 14 Oct 2025 23:03:07 GMT  
		Size: 188.8 MB (188784436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acedfad45cac3565fdd41240e3bd0e4163609c9828507bcc0e6e134330c427a`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-alpine`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.21`

```console
$ docker pull julia@sha256:d1a3e070ace2a47e5eb3cf2e507a090c9b0be78e986d61fa40b7b708e53a3842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:52ac97bc4b7d2863b731985c6614a46e6ab4f13f13f3c8d91d933a5c13055102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181941938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df008c40538a112568d8ff3054242fbabee9d18edd7f08445c7c38cf6f7cea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bda53ebb21b1322cf919f16ba5b28ae9b1d9acd8c0d0da1518623793417c9`  
		Last Modified: Sat, 11 Oct 2025 01:40:30 GMT  
		Size: 178.3 MB (178298998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d772ec346b861be7ae3ae4939fab2ea82732b66bf0931f5d9a7cb217646c0c6`  
		Last Modified: Wed, 08 Oct 2025 23:29:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:9b1b7279a096a1493387b3ed071e6f6201a78ed8dfd3ecc09596e34b48a8e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a9169be517a413e716324eb64afaf1e70b5e4bf29b7ab8205696d41c42cfd`

```dockerfile
```

-	Layers:
	-	`sha256:d87cc8698e0b72551245a2ae783ddb2d064e0bf0c6a2b90e877668ed5777c209`  
		Last Modified: Thu, 09 Oct 2025 02:02:25 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b3221cfc383c0844d2d950de60a17caa749b9d059d4a7e43848dc1f00be791`  
		Last Modified: Thu, 09 Oct 2025 02:02:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.22`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-bookworm`

```console
$ docker pull julia@sha256:71bf8dd5cea601085b5e5bda831ee0ca94cc7c2976fde387c58864630778c1cb
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

### `julia:1.10.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:56ca89a4913111a3df25b7cdc4bc77642f1a1ded3ac43660c2e66a8eefb20c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb98ec8b77011c7171bae247431a414460552e065967960acab8af8463399cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadaf0b1f5567f40dc2814fa5f45c5fa2670bf6c720e01f1b1bdb517f583d8c1`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 5.7 MB (5716321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e569c877561a6133f73a70ff560f923963fcfc6b02b65c269cabecfed2501da3`  
		Last Modified: Tue, 21 Oct 2025 11:05:06 GMT  
		Size: 176.3 MB (176324295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035b022015f0b8155f53e40bf620a31cd1ad80f016826d9c7ef62350e5efa614`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0c263d68101b28aa6c405c25ecd175293e6f2c46a1185d5feb539d4396b950b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0415041bed2d86f2fce6a6b1980599168066c0bbc2ea5c1d322b956ee22b578b`

```dockerfile
```

-	Layers:
	-	`sha256:f7f573e8cc8a009e9c62e2bd525e60fff99fbbc8b820473bab70070bfbbb11f9`  
		Last Modified: Tue, 21 Oct 2025 11:02:49 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2d2dcc3b86e47ba5a4bec6ccd72ff86d3d6e2353e61b52c4190a4e0bb54960`  
		Last Modified: Tue, 21 Oct 2025 11:02:50 GMT  
		Size: 16.6 KB (16641 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c3130bbdfb0559135e7e4fd3ec3ce444ad642a3caa27fb0305ead377a5ba1153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211081933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7e3d3935b40dfd41e295b20c7ab986fd313a3b2dee197f9254afcda97996bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7930cebf84a215d9eb527b9278102385789e575096e6a1a5decc8dc34c5c007f`  
		Last Modified: Tue, 21 Oct 2025 01:20:23 GMT  
		Size: 5.6 MB (5567070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416814b75386b08ccd9efc878f5b1bc15709a2a71fc3ffebd1a092d755e9f1d3`  
		Last Modified: Wed, 22 Oct 2025 12:39:10 GMT  
		Size: 177.4 MB (177412306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89f0b4eeb4bf4a2193878aceff84d44746dccf95da007ea8629584b3a9b027`  
		Last Modified: Tue, 21 Oct 2025 01:21:25 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a6b95972daf4e0e6df5ce08df964d84009b03bde5ba141c8a45acf6969ecd8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd6d40a3535c364489348457caf353b2c83f97b5cc3beae4e369728b71ea11b`

```dockerfile
```

-	Layers:
	-	`sha256:0e9c1065e40271bc546b2304d9b2243d96d16a0da5ebf5231b5e335ae02cc761`  
		Last Modified: Tue, 21 Oct 2025 08:02:29 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3355becbc13b4ce3459da9b6c637c6d87c240b5733b9001efe32a4756681cc`  
		Last Modified: Tue, 21 Oct 2025 08:02:30 GMT  
		Size: 16.7 KB (16735 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:179ebe72059e625727a4736be24707996f49692aecc554661434ddb340887238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192895973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855ca2f4f13088b54f82af4e38f806fb3c1d764e3afbf57540d1fc3e561afae6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ab4918e431ea323c9daec4dafe9801c0dd4b05fcfd38b1b494a2ba0b322325`  
		Last Modified: Tue, 21 Oct 2025 01:19:29 GMT  
		Size: 5.9 MB (5878032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cffbc8da390394fd981f2bd70983ba3930f30f9bcf7fb3e2b2f015829fc812a`  
		Last Modified: Tue, 21 Oct 2025 01:19:21 GMT  
		Size: 157.8 MB (157807895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69545198becd2e773efc013832bbf758d85363e6493e2cd377e0e148664e806d`  
		Last Modified: Tue, 21 Oct 2025 01:19:28 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8b88744c754dc4bb32d6c0826aa999a64d05129cbe02424cf799ed5ec2696df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a892247c2c5f8fac45878c6db509c9d11dcf18e1ccdbd51da473db035cd2f0`

```dockerfile
```

-	Layers:
	-	`sha256:1a9a6f23d48d24ef5021b38a903e06500289bec5d1f666ac4166e7bfaa9c5859`  
		Last Modified: Tue, 21 Oct 2025 11:02:56 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d25c997bf28e7be184be14f9e2940b8e9d9c32220ab6845f810fe4f7d8f647`  
		Last Modified: Tue, 21 Oct 2025 11:02:57 GMT  
		Size: 16.6 KB (16617 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:82ae3c194c2009ca9f2a8edadc20a231612fefa360b5f7be0cca2cb8ad8cc32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f03ee3ded076f2fdbe02b9bc806a7f5a7f0557774745d081a7ce044661e0db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc155374c7db12d97ec8dfc57f566dd402662f9a5876305b298bced2fb30309b`  
		Last Modified: Tue, 21 Oct 2025 01:46:55 GMT  
		Size: 6.3 MB (6256276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da959eb093540b25d0974705d27b2eaa0cf9bb54738f3bfb11b917259e8b9d1`  
		Last Modified: Tue, 21 Oct 2025 01:50:42 GMT  
		Size: 155.4 MB (155354835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fce20b9476a27fed9f408abf77260dba6eb85cb99d1c7499f41f28e59df296`  
		Last Modified: Tue, 21 Oct 2025 01:50:51 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0751301f06b4a89e7a7a7ba740c617e1e99d0062078016608867ea197e876cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6084b56427bb65bc0f5e8cf66115b42d6b33773b8829a3387f7052450c48ced`

```dockerfile
```

-	Layers:
	-	`sha256:ff6bdc2ae85d9e0d9900bf628e28fc7ae8a6b063fad4e15def017dfa29ce7a63`  
		Last Modified: Tue, 21 Oct 2025 05:02:36 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbd4e35b3f2cbb7994174ca2d996f998336c04399b864fac7c5af1d42e33372`  
		Last Modified: Tue, 21 Oct 2025 05:02:37 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-trixie`

```console
$ docker pull julia@sha256:e775b60db76f95d737365d8964a2bf5e66e8187e6fd6bc631f318dc6fe4a7974
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

### `julia:1.10.10-trixie` - linux; amd64

```console
$ docker pull julia@sha256:171e8a5fc64c8acf452dc5eb8e35867048f7b52e396bd2f8d9bb32879dfb78ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c0dc3eeeb6d983dfd6b11756d830ec08a7e15a67f4df66b55c48fb2121da6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b6514be2fdb4df0784d0c6d265b9736a3fda7dc8d3278c5fadc3f460411b6e`  
		Last Modified: Tue, 21 Oct 2025 01:29:39 GMT  
		Size: 6.2 MB (6242721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8376bab843477c63f1a903e9052f5423c1f32ad5281d38f365b21283194328`  
		Last Modified: Tue, 21 Oct 2025 11:18:47 GMT  
		Size: 176.4 MB (176362186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a312a0b56be934b80a01b6e9b5df17eae9ad346528db3259e0038063290e27e9`  
		Last Modified: Tue, 21 Oct 2025 01:29:38 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:e6249fd9e30017ec06d8dd6d0ef078272e8590671d2e9cd9d8ca784d0d71ba9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34252a4fad6d01efee29409a60454f1b7aee539b6c4552495094cffa4686d0f6`

```dockerfile
```

-	Layers:
	-	`sha256:f685c3ef5f9352c3b371bdb93706b3d6f6d280753caf841f4e069e1985a6590f`  
		Last Modified: Tue, 21 Oct 2025 11:02:40 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4e605a73c3f29f0f7d53882a0e566bb0e3a86955889a4e14ad74d1cf10bed6`  
		Last Modified: Tue, 21 Oct 2025 11:02:42 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:0239f692dba1d0d42c19d420ec672a7b3601db65eab9920cdcfba5bf48fc0b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213745597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc5428e2fd7f01fd8e5ee155bd30a40152186bfb01a317e4a2fa5a2d813bf88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38525cd6f78da9fe5917c1c21169e062879af73a6472e7ac9963d8f2b1463f7`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6153026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a6c2ef61011ed5ba1789ce07901841387015b024de528eeaaf76847b08137`  
		Last Modified: Tue, 21 Oct 2025 09:59:26 GMT  
		Size: 177.5 MB (177450078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e9f69a7f3d5115598c06e2d346fe6be0774b3bd22f47727a24a51354b8563b`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b4a936149a26a183114c94639fddc55d39ff48461c48565e880b87e3f09a8172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927cad95cf4f15f1f52a85791a409dc0f4ad0c6aeacfbfcec497d42459d60c5f`

```dockerfile
```

-	Layers:
	-	`sha256:c19d85ca0548f0d6cc587c82286ca6693f42d10b632606d173ee6cba564965b5`  
		Last Modified: Tue, 21 Oct 2025 08:02:22 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2971538095a08b1b1da12832e3c5f1958d99ef1da1e4ea3d1e8b4f837f2a91`  
		Last Modified: Tue, 21 Oct 2025 08:02:23 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:0705758aeb67f7bc90ad7a7bb8179e31aac2a3f0bde668724f4174a77b4aab38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c3565aaac74483ba08f8641f67ec87282809e1490714b7fc50a5b5cec8fcc0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f966b3cc15e4cb49ec9bb8df24e0c88bf15746ebae8548e96fbbb93633d5a0`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44a8e7fa3869efc4a509f98572ab506e421276af500708f787443aeb4400def`  
		Last Modified: Tue, 21 Oct 2025 01:19:05 GMT  
		Size: 157.8 MB (157841879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8662b7f81de827a3380f5546b30129577c4fcaf02c72239deaa89310944f066e`  
		Last Modified: Tue, 21 Oct 2025 01:19:21 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2391cd75f75437374cbddad89f0aab02de737b669a4ebe28a23ee2f9710b0b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b755542b72a9aa98ad7d3ae120b8300ea1003802d0de7a58d42a814267f72a57`

```dockerfile
```

-	Layers:
	-	`sha256:76ff8ca1e4dc815578aad8ddca8aaa4626192cb6eb1d5fa0df79c4002f4dd6e6`  
		Last Modified: Tue, 21 Oct 2025 11:02:48 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52a1c40a1578f4d68aafdd9c1a4d827a59508836bbfc310e97d1c57fbd7554fd`  
		Last Modified: Tue, 21 Oct 2025 11:02:49 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:4042a0d68db8686e48335f06fcc6cdceb2fe96d045c847c4461513df0a0f261f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c44f202b74bfeffe7433cb8c2a25e796e490a54062a438c29cb9c6ea313bb74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 08 Aug 2025 17:33:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 08 Aug 2025 17:33:54 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 08 Aug 2025 17:33:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 17:33:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 17:33:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8da13a7f27803c776568aca71a6cabc5ddf5ed82c2f7cc0348cd05e52debf21`  
		Last Modified: Tue, 21 Oct 2025 03:58:38 GMT  
		Size: 155.4 MB (155388365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c84e2e6978ed83fb08cd18bed60c508f9de0b5ef024d15b3c434d21a14364f`  
		Last Modified: Tue, 21 Oct 2025 02:02:53 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:16d7d83e82171e92042a8795fdb8148f328b7e08f36c96621362d47e3b3f6229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab92b9c43318187ad5dd7ffb7b1d71fe446bd86ab76cea2a750fa3b54b70c393`

```dockerfile
```

-	Layers:
	-	`sha256:62cecf066859dea5b0321d01b076a4fae44ae56c8849a76033ed07391898f966`  
		Last Modified: Tue, 21 Oct 2025 05:02:30 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5830d2c56244f939e74422344e6958eb6f885bfb31f1ad7919bcd39fd14ff56e`  
		Last Modified: Tue, 21 Oct 2025 05:02:31 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-windowsservercore`

```console
$ docker pull julia@sha256:3de3c91fc7e43489691d08752394eb872add49cabf2362dc48d91b86051dfed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.10.10-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:f3c97d1e2d7fb192166f1dfa792a121d59a247380a8984016ff1bb3a2b110743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409264907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8aed3f999fce7f0dc4ceeecb0c032760cb299b77698d9f674f7e5a09c57e14`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:43:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:44:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c51f38aa013c2055a61a5f4a1d2349666eb9457e574fe677c96bbd46b9e55c`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe1604df2b99eba86d1d80ece03ad84ea7917e7b33cdb0a9b84f01b3347255`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72b26b1d61f16966ff8b108660abe3e3ab028e7d36a5c65aaed346bdbea6b8`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa9b25d3173de6f519caeb4758cd9ff20b540b49cd40f5f366e05f6c37d472b`  
		Last Modified: Tue, 14 Oct 2025 21:36:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b3b144bcb26e0de9b8c8a5e7bc278cbed04696d69a361e6a1344302aa957f`  
		Last Modified: Tue, 14 Oct 2025 23:03:11 GMT  
		Size: 188.8 MB (188777893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf54f68dc216b1db2632a56ce7266059422ed1c29e8b8beb236ba9ff78977ce`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:468da5ad969609da851733e9c20b4fdbebea12f1386f1c8175c60f364133ac8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1677810088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e08269a98333beb3e137791613a7adb2ea0c4cf0c67a9c0e1eab434a3972a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:43:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5601680face9cd24ed8439d5d819578a5a6e960e1c1890e9c1038facd81b9ee`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb5079dc730813a1d1f566cd6f3636b3d1959c605a6340200181dd8d2c546ac`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653aa7f3d49f56c710d8b384f0aaaadfc59990fdee5a76d0ffd7cec6cfc3d10e`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedccef22ecdcd576e671f208da349b7493e2a1ddcb624a5aadf2c6ce3b436b`  
		Last Modified: Tue, 14 Oct 2025 23:03:07 GMT  
		Size: 188.8 MB (188784436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acedfad45cac3565fdd41240e3bd0e4163609c9828507bcc0e6e134330c427a`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:6a4c454e6a05b7c84ff96eff12eae0db007d22e2fba00b72ddf48222b5ea0bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1.10.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:468da5ad969609da851733e9c20b4fdbebea12f1386f1c8175c60f364133ac8f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1677810088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e08269a98333beb3e137791613a7adb2ea0c4cf0c67a9c0e1eab434a3972a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:42:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:42:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:42:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:43:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66372537236e118b52127079b58ddc2c73994a97b7e24f173a5a8cc1b638279d`  
		Last Modified: Tue, 14 Oct 2025 21:12:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5601680face9cd24ed8439d5d819578a5a6e960e1c1890e9c1038facd81b9ee`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb5079dc730813a1d1f566cd6f3636b3d1959c605a6340200181dd8d2c546ac`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653aa7f3d49f56c710d8b384f0aaaadfc59990fdee5a76d0ffd7cec6cfc3d10e`  
		Last Modified: Tue, 14 Oct 2025 21:34:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afedccef22ecdcd576e671f208da349b7493e2a1ddcb624a5aadf2c6ce3b436b`  
		Last Modified: Tue, 14 Oct 2025 23:03:07 GMT  
		Size: 188.8 MB (188784436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acedfad45cac3565fdd41240e3bd0e4163609c9828507bcc0e6e134330c427a`  
		Last Modified: Tue, 14 Oct 2025 21:34:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:1e3df351c3942a018cb4879d6c45d76830c9ca55e1ba5f737932eb92fed1dfef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1.10.10-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:f3c97d1e2d7fb192166f1dfa792a121d59a247380a8984016ff1bb3a2b110743
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409264907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8aed3f999fce7f0dc4ceeecb0c032760cb299b77698d9f674f7e5a09c57e14`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 14 Oct 2025 20:43:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 14 Oct 2025 20:43:51 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 14 Oct 2025 20:44:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c51f38aa013c2055a61a5f4a1d2349666eb9457e574fe677c96bbd46b9e55c`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe1604df2b99eba86d1d80ece03ad84ea7917e7b33cdb0a9b84f01b3347255`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a72b26b1d61f16966ff8b108660abe3e3ab028e7d36a5c65aaed346bdbea6b8`  
		Last Modified: Tue, 14 Oct 2025 21:36:50 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa9b25d3173de6f519caeb4758cd9ff20b540b49cd40f5f366e05f6c37d472b`  
		Last Modified: Tue, 14 Oct 2025 21:36:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b3b144bcb26e0de9b8c8a5e7bc278cbed04696d69a361e6a1344302aa957f`  
		Last Modified: Tue, 14 Oct 2025 23:03:11 GMT  
		Size: 188.8 MB (188777893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cf54f68dc216b1db2632a56ce7266059422ed1c29e8b8beb236ba9ff78977ce`  
		Last Modified: Tue, 14 Oct 2025 21:36:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:64c90010e9be1f8b600297ccbd16b520337f0779cb96db055cd373da95c150a6
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
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:c1a4b7d7f398db0f3689848c5d5d4830aaaf5b028aa8a2d22636a78caf6a28b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050b786f30db3e872c49ef9e199a3f8e998c1d376d7489b833672fb43a1992c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f197fd3303ab25f3f09540cc089e3f5efc0d2c3da24f72515e1ef2120013e3f`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6242779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd2d9030da9c64039ed492740b7e2d81ef2293cb1d32ccc1e95fd3040adc2e7`  
		Last Modified: Tue, 21 Oct 2025 11:08:58 GMT  
		Size: 288.8 MB (288825612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4693ebdb3345b02a5895e8ce2151682eb3f2ce609c793798769903f3c49d0`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:1e39a89eaaa73274a6235ddaf1ea96fafcff9d95d94f7ee271383de31c2e941a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd953062c4bf43dba26149d26978e48666f70f3a2b391f828f00c936ba07468d`

```dockerfile
```

-	Layers:
	-	`sha256:8bb944154d3357a7cfd615409baa93815f6df29df973ef0a4f61b14e20ec7b51`  
		Last Modified: Tue, 21 Oct 2025 11:03:13 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c2157a84659528c287b0c20d002b412df2944c6f26949ca459730287a5fe0a`  
		Last Modified: Tue, 21 Oct 2025 11:03:14 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:28a6633dde0f2f68ef34736e32d02465e7d8fc358a85a93aab0d4dc1a47d1f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc88ee5486f116ff82337aa3d80476c96f998f9595d724cc3b796946ef0fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7317e038a5aee60731ca3e760aa1c072354ae7d86ead1c4a3e12e9868f7ce90`  
		Last Modified: Tue, 21 Oct 2025 01:20:40 GMT  
		Size: 6.2 MB (6153023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd99a31f1a641fb61386055fbb8250f82030ee4c2e3412c994d2eacffdeb3b3`  
		Last Modified: Tue, 21 Oct 2025 11:29:01 GMT  
		Size: 304.7 MB (304672756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e973a1c1d9ab3b9d844abfd958960f0a9c4ed26a5c600b14d016adf4aa40a2`  
		Last Modified: Tue, 21 Oct 2025 01:20:39 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:2356356811d039bbbbdda5867ba0b5c0e7e385c3385e20c223d9c7f4a64207d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eddab6c164ab8e6448636761f0d405cc20b2ddb207abd5d2bb5b547bf8b2536`

```dockerfile
```

-	Layers:
	-	`sha256:fc73fc6e0e142e936163c7d3d63c5e4a834fb75a9c39ad3783608321478d2116`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63968c49ec46ef1596ec92911d27817eeb8d6a499929946eeee0629b1574c868`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 17.3 KB (17311 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:08851af22580d93edcff7af3400be7e451b3c74212780b4ccbab945dc0490f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301e3c68d9dab1a6c4102cc12904224ec14a689888175c58a3a0e74262374512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82545143988a5b43a1ac2b12be33d25c56903bb53a03c874f94074c56b82a9b2`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351580ccf1dcf1a05929fbb2822da43ba07255858a16167c7f816b5ebbc3bf3c`  
		Last Modified: Tue, 21 Oct 2025 21:50:05 GMT  
		Size: 237.6 MB (237589422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe17231b8108ee61fd58d12753ee11dec04c8c4e624108143ca7c284992c8de2`  
		Last Modified: Tue, 21 Oct 2025 01:19:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:7b9c5956245f1fea910d1714286310c78b6f9960efecdfb110461db882b01c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c96af9338b16a0e8ff0307467a6d0969dd848f75d42518d302919e0739305`

```dockerfile
```

-	Layers:
	-	`sha256:ca90562f0fd69376a215aaa90862d09081ee1ca8d926fd3bcaf4ba112ace9079`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58959592db46a248dc7122be1982bd94898c8b62ee559d96c9ae9a52185cc8c9`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 17.2 KB (17160 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:377c2602ad24e8f8df7425b947a50638aa20d4d2ff30ee7ab4f132be6a141e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41467295ab7ebac3684a2b2219084b17cd805ea7d5c331d7cf7b46812ea8906a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4f1de44718b36ed847bbbe4de338299d54a379fd71d6e6711dbb508570f510`  
		Last Modified: Tue, 21 Oct 2025 03:19:57 GMT  
		Size: 248.6 MB (248575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b937d93623990522216e1a0a83563425b4bb035cc4fa7ba6518c5ecc656d6`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:ddcd0937fb9cd450bb6dd81818867007e0222dfb2d12fafc3a1d44a0e412f67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17df2b6d907f57a694f30a0fd0f4b56c9cdb66360cee6ce262e2a3eaf5ba10`

```dockerfile
```

-	Layers:
	-	`sha256:efd875ebfd2967cbd9fd6c4bed7870805f9b888d456bcad1b571b1b3520936ac`  
		Last Modified: Tue, 21 Oct 2025 05:02:57 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d6c66e1cfab9ac54308f4f346503af7acd961b26f76c2142125061e2eb0573`  
		Last Modified: Tue, 21 Oct 2025 05:02:58 GMT  
		Size: 17.2 KB (17239 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:1a26e88a17bdfdb85336d88383e56217f386aa2458676363dcf66072d20ed1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506557781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe16003af3c162062c3b364cb4e0c9cfb350e841279e4aaeb8e65d76f7f6eab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:43:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:43:37 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:44:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f414e59fea2048693dfebf404f4ad0f980c980b1774cb29ae48cc293dd33cd`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9d16d2eefa04feecc234db6c45927164decd790dcdd12fb716ca2beaadb07`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85f34eaa04a9aa73ff9476f42d2ea1c1e0a81f2403fd0ab0a984c50143d1532`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372d9a32a2c3449d272982caa4939a2adaf2f9bce070d0fee80a4725299c6b0`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303deec3a031d89d2bd2b09857919b270db4130e539c4e69330fadc67f78f0c5`  
		Last Modified: Tue, 14 Oct 2025 23:03:58 GMT  
		Size: 286.1 MB (286070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f687bcae71dc1fe0ac3cd6c1aa42dcb4a88e4fce99d355839f214a46d5662ae3`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:1f3f5edaf659bb79ee9e91066a344f5b1796329dcd7601db9f44d9653c661cae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775034330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e10ce22e24661a2ecb8050770be373b4eefa519b740957ca350171909ddbee`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:59 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:43:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f81acf066b453e930a52b0f1cbd7f822cd50c543225d7d9cf6f16d51a27255`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cd4f5df3257e4533b67d0ccb0560ba0f1313540ceea39b1ceff9f2322981c`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c053e3eb854dea2a46d6194563ddf72979e2bccfda2c5c736035b0886ff4d`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6cb154dcd3209f47f3091b30e06342f360e4005b13509076d3436f421c3a5`  
		Last Modified: Tue, 14 Oct 2025 23:03:51 GMT  
		Size: 286.0 MB (286008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b2c48116adac832a87d095f7d2549732df53cc9dcce97fd0c11f83671dc97`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:1c0532da44349210e82ada44882147cbb75ff897b322aa3bacaa0f57319ba34e
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
$ docker pull julia@sha256:398039db5bcace9e4f649ca5c1f6d03710f1995695b132dc827201175e862fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a193a1343cfc53434d6bd9fd5b67df4ea3baaa50c98ba98e454d0d1d2b302d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdacae64ad0ef312a8abbda8255aac0b873c406d849f5eba98857d3dddd20f28`  
		Last Modified: Tue, 21 Oct 2025 01:21:32 GMT  
		Size: 5.7 MB (5716297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56b41b941f9ddd8d84273ae5ad9b846f2a03a7fae1b459e59c6599fd5d5894`  
		Last Modified: Tue, 21 Oct 2025 14:10:27 GMT  
		Size: 288.8 MB (288788417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c01cbd534d4c3dd55640902025206b8896c0df6d9f44113850b9b2126f62ad`  
		Last Modified: Tue, 21 Oct 2025 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3650991c616122ed087a94a68308548aaff36007e55893b3aabfd6969b7107ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883afbac5f0beeca3142fefdb1ec3d0667285934a14297eb605f1557529505de`

```dockerfile
```

-	Layers:
	-	`sha256:6cc113a566ee9958f6f3cb8cc09cf9fdb24905b0159b9b90d7a384fe8ef67e05`  
		Last Modified: Tue, 21 Oct 2025 11:03:20 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2965f1a9014ae6d8430c59a6491f9dcd3378968fcfb3a913cd6d17737fdbab`  
		Last Modified: Tue, 21 Oct 2025 11:03:21 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:737aa5901a76684a1f4666e30afbb82c3227e746aebf299f0e305b504ecc1e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e572b897e07c49f1ec159d2b0f1c56e34b242aaca37d4b58a4b4c7981f9d8ac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d42b8b1a5aa2fe59b952ee689d785a46622ca0391174ce91c42d91899bc89`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 5.6 MB (5567093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8f62164c7192264de3339454f1c6c6a243f796044cc3474a89462f3b0be96`  
		Last Modified: Tue, 21 Oct 2025 13:40:24 GMT  
		Size: 304.6 MB (304646608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2f80538f06795371953bf234659723cb1c33d24b497e04b41859ff308f4e1b`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ce21f54d92e8718caa367a8f5ddb0145c1da39c1a8a4cc7beed93cea5d189f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a4da0ffeb51f06d52085195f53b944fbac74d1554c37f4798a03991b5aa4e1`

```dockerfile
```

-	Layers:
	-	`sha256:a190f5f3f7baf0187988a461b52c46fb35a44a4d167bd80b4707219e80a6caf4`  
		Last Modified: Tue, 21 Oct 2025 08:02:47 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d546c395b1b0929bbb64c3e328421ab71127ae8b64a7dbcebb8c572fa162bf67`  
		Last Modified: Tue, 21 Oct 2025 08:02:48 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d1e478f72f6cc935fff064fe14e5bd0bf3e776b273539bc2d4d8f612cdc683f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff414cd59f151e142d5c053e97f892d63eb8a104a8381512588576e4cf9dc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a912b6853a709cb605792534a8ef346eb642e19cbf2604744511031a9a2e2313`  
		Last Modified: Tue, 21 Oct 2025 01:19:27 GMT  
		Size: 5.9 MB (5878012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ba8de8917734655b769288eeb6524c9c45e7806aba867500e1689cd7df68b`  
		Last Modified: Tue, 21 Oct 2025 02:55:45 GMT  
		Size: 237.6 MB (237555799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae7fd496f776220d47329c8602768c58a5c87ef69e0881d70fcbd0cd563fae7`  
		Last Modified: Tue, 21 Oct 2025 01:19:27 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:34b0241daf94d698a79d88f4e4e797e1ac314a7b706a1000569356eb19fbdcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6beb3a9c8569c651cf07d8a62e48aa7b53746207728b7afd8f70d6aadc233a`

```dockerfile
```

-	Layers:
	-	`sha256:f9fc4ad5c7c17855ef666449ae6824c46c5952f454996fb8c6701a15d902babd`  
		Last Modified: Tue, 21 Oct 2025 11:03:28 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839790cb167df012aea9492c6fc9cf41e1c009fccbe560874552b6b04c7e7798`  
		Last Modified: Tue, 21 Oct 2025 11:03:29 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:9d83aae3c9991b3b389f9f1619a6fd0a3c3c3cb95458a1fb44d35e7e9e693eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed8a4b359c462a5e9ca88c84c5ce2500ae1af93ece83e82cfe0d9ac806fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc155374c7db12d97ec8dfc57f566dd402662f9a5876305b298bced2fb30309b`  
		Last Modified: Tue, 21 Oct 2025 01:46:55 GMT  
		Size: 6.3 MB (6256276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483cbf9a6fcd9f801cefe9174ac90d0c3273a5cedbed0d5eebab73acf38e6ef8`  
		Last Modified: Tue, 21 Oct 2025 01:46:49 GMT  
		Size: 248.6 MB (248553870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8adfaf14441b4b616dee5f105ce1ee2405f230ab9656420573232387a87301`  
		Last Modified: Tue, 21 Oct 2025 01:46:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:92ee77a70b5f5f83f876488fba8a581b470d7d6bc17058ca4b81434e937471a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27822b8ba478a2ba49d504824a1a9c6dfe020fc21bb6700e76cc514f222f09f7`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5f0499d02236fa1a7e5da9b344f97ff0403082333a6d2b351c89f82ffbc0b`  
		Last Modified: Tue, 21 Oct 2025 05:03:02 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f262c2e27264305d1c1eada818f6f98cf9d1bee310fe288e848f695d3a11d38`  
		Last Modified: Tue, 21 Oct 2025 05:03:03 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-trixie`

```console
$ docker pull julia@sha256:520a0e46bd2574ba4d96e4fd6e5ecde251f2258645730566ba1d6da4faa8c3ff
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

### `julia:1.11-trixie` - linux; amd64

```console
$ docker pull julia@sha256:c1a4b7d7f398db0f3689848c5d5d4830aaaf5b028aa8a2d22636a78caf6a28b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050b786f30db3e872c49ef9e199a3f8e998c1d376d7489b833672fb43a1992c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f197fd3303ab25f3f09540cc089e3f5efc0d2c3da24f72515e1ef2120013e3f`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6242779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd2d9030da9c64039ed492740b7e2d81ef2293cb1d32ccc1e95fd3040adc2e7`  
		Last Modified: Tue, 21 Oct 2025 11:08:58 GMT  
		Size: 288.8 MB (288825612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4693ebdb3345b02a5895e8ce2151682eb3f2ce609c793798769903f3c49d0`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1e39a89eaaa73274a6235ddaf1ea96fafcff9d95d94f7ee271383de31c2e941a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd953062c4bf43dba26149d26978e48666f70f3a2b391f828f00c936ba07468d`

```dockerfile
```

-	Layers:
	-	`sha256:8bb944154d3357a7cfd615409baa93815f6df29df973ef0a4f61b14e20ec7b51`  
		Last Modified: Tue, 21 Oct 2025 11:03:13 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c2157a84659528c287b0c20d002b412df2944c6f26949ca459730287a5fe0a`  
		Last Modified: Tue, 21 Oct 2025 11:03:14 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:28a6633dde0f2f68ef34736e32d02465e7d8fc358a85a93aab0d4dc1a47d1f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc88ee5486f116ff82337aa3d80476c96f998f9595d724cc3b796946ef0fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7317e038a5aee60731ca3e760aa1c072354ae7d86ead1c4a3e12e9868f7ce90`  
		Last Modified: Tue, 21 Oct 2025 01:20:40 GMT  
		Size: 6.2 MB (6153023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd99a31f1a641fb61386055fbb8250f82030ee4c2e3412c994d2eacffdeb3b3`  
		Last Modified: Tue, 21 Oct 2025 11:29:01 GMT  
		Size: 304.7 MB (304672756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e973a1c1d9ab3b9d844abfd958960f0a9c4ed26a5c600b14d016adf4aa40a2`  
		Last Modified: Tue, 21 Oct 2025 01:20:39 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2356356811d039bbbbdda5867ba0b5c0e7e385c3385e20c223d9c7f4a64207d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eddab6c164ab8e6448636761f0d405cc20b2ddb207abd5d2bb5b547bf8b2536`

```dockerfile
```

-	Layers:
	-	`sha256:fc73fc6e0e142e936163c7d3d63c5e4a834fb75a9c39ad3783608321478d2116`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63968c49ec46ef1596ec92911d27817eeb8d6a499929946eeee0629b1574c868`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 17.3 KB (17311 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; 386

```console
$ docker pull julia@sha256:08851af22580d93edcff7af3400be7e451b3c74212780b4ccbab945dc0490f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301e3c68d9dab1a6c4102cc12904224ec14a689888175c58a3a0e74262374512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82545143988a5b43a1ac2b12be33d25c56903bb53a03c874f94074c56b82a9b2`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351580ccf1dcf1a05929fbb2822da43ba07255858a16167c7f816b5ebbc3bf3c`  
		Last Modified: Tue, 21 Oct 2025 21:50:05 GMT  
		Size: 237.6 MB (237589422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe17231b8108ee61fd58d12753ee11dec04c8c4e624108143ca7c284992c8de2`  
		Last Modified: Tue, 21 Oct 2025 01:19:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7b9c5956245f1fea910d1714286310c78b6f9960efecdfb110461db882b01c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c96af9338b16a0e8ff0307467a6d0969dd848f75d42518d302919e0739305`

```dockerfile
```

-	Layers:
	-	`sha256:ca90562f0fd69376a215aaa90862d09081ee1ca8d926fd3bcaf4ba112ace9079`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58959592db46a248dc7122be1982bd94898c8b62ee559d96c9ae9a52185cc8c9`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 17.2 KB (17160 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:377c2602ad24e8f8df7425b947a50638aa20d4d2ff30ee7ab4f132be6a141e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41467295ab7ebac3684a2b2219084b17cd805ea7d5c331d7cf7b46812ea8906a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4f1de44718b36ed847bbbe4de338299d54a379fd71d6e6711dbb508570f510`  
		Last Modified: Tue, 21 Oct 2025 03:19:57 GMT  
		Size: 248.6 MB (248575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b937d93623990522216e1a0a83563425b4bb035cc4fa7ba6518c5ecc656d6`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ddcd0937fb9cd450bb6dd81818867007e0222dfb2d12fafc3a1d44a0e412f67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17df2b6d907f57a694f30a0fd0f4b56c9cdb66360cee6ce262e2a3eaf5ba10`

```dockerfile
```

-	Layers:
	-	`sha256:efd875ebfd2967cbd9fd6c4bed7870805f9b888d456bcad1b571b1b3520936ac`  
		Last Modified: Tue, 21 Oct 2025 05:02:57 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d6c66e1cfab9ac54308f4f346503af7acd961b26f76c2142125061e2eb0573`  
		Last Modified: Tue, 21 Oct 2025 05:02:58 GMT  
		Size: 17.2 KB (17239 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:d9cfd001c2470fe693f01e5cf111d84115fd23409931fa881e9fd54ed7581286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:1a26e88a17bdfdb85336d88383e56217f386aa2458676363dcf66072d20ed1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506557781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe16003af3c162062c3b364cb4e0c9cfb350e841279e4aaeb8e65d76f7f6eab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:43:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:43:37 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:44:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f414e59fea2048693dfebf404f4ad0f980c980b1774cb29ae48cc293dd33cd`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9d16d2eefa04feecc234db6c45927164decd790dcdd12fb716ca2beaadb07`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85f34eaa04a9aa73ff9476f42d2ea1c1e0a81f2403fd0ab0a984c50143d1532`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372d9a32a2c3449d272982caa4939a2adaf2f9bce070d0fee80a4725299c6b0`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303deec3a031d89d2bd2b09857919b270db4130e539c4e69330fadc67f78f0c5`  
		Last Modified: Tue, 14 Oct 2025 23:03:58 GMT  
		Size: 286.1 MB (286070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f687bcae71dc1fe0ac3cd6c1aa42dcb4a88e4fce99d355839f214a46d5662ae3`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:1f3f5edaf659bb79ee9e91066a344f5b1796329dcd7601db9f44d9653c661cae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775034330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e10ce22e24661a2ecb8050770be373b4eefa519b740957ca350171909ddbee`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:59 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:43:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f81acf066b453e930a52b0f1cbd7f822cd50c543225d7d9cf6f16d51a27255`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cd4f5df3257e4533b67d0ccb0560ba0f1313540ceea39b1ceff9f2322981c`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c053e3eb854dea2a46d6194563ddf72979e2bccfda2c5c736035b0886ff4d`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6cb154dcd3209f47f3091b30e06342f360e4005b13509076d3436f421c3a5`  
		Last Modified: Tue, 14 Oct 2025 23:03:51 GMT  
		Size: 286.0 MB (286008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b2c48116adac832a87d095f7d2549732df53cc9dcce97fd0c11f83671dc97`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:776b1833a5b24002caee933bc1b5e86569c94efdb02be89e80a09c76080c8bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:1f3f5edaf659bb79ee9e91066a344f5b1796329dcd7601db9f44d9653c661cae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775034330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e10ce22e24661a2ecb8050770be373b4eefa519b740957ca350171909ddbee`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:59 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:43:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f81acf066b453e930a52b0f1cbd7f822cd50c543225d7d9cf6f16d51a27255`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cd4f5df3257e4533b67d0ccb0560ba0f1313540ceea39b1ceff9f2322981c`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c053e3eb854dea2a46d6194563ddf72979e2bccfda2c5c736035b0886ff4d`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6cb154dcd3209f47f3091b30e06342f360e4005b13509076d3436f421c3a5`  
		Last Modified: Tue, 14 Oct 2025 23:03:51 GMT  
		Size: 286.0 MB (286008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b2c48116adac832a87d095f7d2549732df53cc9dcce97fd0c11f83671dc97`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:e904e07585d5ea8cc8c94a69eee35d81a0083b58a974feec1a81ebaaf6f69abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:1a26e88a17bdfdb85336d88383e56217f386aa2458676363dcf66072d20ed1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506557781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe16003af3c162062c3b364cb4e0c9cfb350e841279e4aaeb8e65d76f7f6eab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:43:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:43:37 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:44:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f414e59fea2048693dfebf404f4ad0f980c980b1774cb29ae48cc293dd33cd`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9d16d2eefa04feecc234db6c45927164decd790dcdd12fb716ca2beaadb07`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85f34eaa04a9aa73ff9476f42d2ea1c1e0a81f2403fd0ab0a984c50143d1532`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372d9a32a2c3449d272982caa4939a2adaf2f9bce070d0fee80a4725299c6b0`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303deec3a031d89d2bd2b09857919b270db4130e539c4e69330fadc67f78f0c5`  
		Last Modified: Tue, 14 Oct 2025 23:03:58 GMT  
		Size: 286.1 MB (286070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f687bcae71dc1fe0ac3cd6c1aa42dcb4a88e4fce99d355839f214a46d5662ae3`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7`

```console
$ docker pull julia@sha256:64c90010e9be1f8b600297ccbd16b520337f0779cb96db055cd373da95c150a6
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
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.11.7` - linux; amd64

```console
$ docker pull julia@sha256:c1a4b7d7f398db0f3689848c5d5d4830aaaf5b028aa8a2d22636a78caf6a28b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050b786f30db3e872c49ef9e199a3f8e998c1d376d7489b833672fb43a1992c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f197fd3303ab25f3f09540cc089e3f5efc0d2c3da24f72515e1ef2120013e3f`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6242779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd2d9030da9c64039ed492740b7e2d81ef2293cb1d32ccc1e95fd3040adc2e7`  
		Last Modified: Tue, 21 Oct 2025 11:08:58 GMT  
		Size: 288.8 MB (288825612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4693ebdb3345b02a5895e8ce2151682eb3f2ce609c793798769903f3c49d0`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:1e39a89eaaa73274a6235ddaf1ea96fafcff9d95d94f7ee271383de31c2e941a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd953062c4bf43dba26149d26978e48666f70f3a2b391f828f00c936ba07468d`

```dockerfile
```

-	Layers:
	-	`sha256:8bb944154d3357a7cfd615409baa93815f6df29df973ef0a4f61b14e20ec7b51`  
		Last Modified: Tue, 21 Oct 2025 11:03:13 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c2157a84659528c287b0c20d002b412df2944c6f26949ca459730287a5fe0a`  
		Last Modified: Tue, 21 Oct 2025 11:03:14 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:28a6633dde0f2f68ef34736e32d02465e7d8fc358a85a93aab0d4dc1a47d1f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc88ee5486f116ff82337aa3d80476c96f998f9595d724cc3b796946ef0fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7317e038a5aee60731ca3e760aa1c072354ae7d86ead1c4a3e12e9868f7ce90`  
		Last Modified: Tue, 21 Oct 2025 01:20:40 GMT  
		Size: 6.2 MB (6153023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd99a31f1a641fb61386055fbb8250f82030ee4c2e3412c994d2eacffdeb3b3`  
		Last Modified: Tue, 21 Oct 2025 11:29:01 GMT  
		Size: 304.7 MB (304672756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e973a1c1d9ab3b9d844abfd958960f0a9c4ed26a5c600b14d016adf4aa40a2`  
		Last Modified: Tue, 21 Oct 2025 01:20:39 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:2356356811d039bbbbdda5867ba0b5c0e7e385c3385e20c223d9c7f4a64207d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eddab6c164ab8e6448636761f0d405cc20b2ddb207abd5d2bb5b547bf8b2536`

```dockerfile
```

-	Layers:
	-	`sha256:fc73fc6e0e142e936163c7d3d63c5e4a834fb75a9c39ad3783608321478d2116`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63968c49ec46ef1596ec92911d27817eeb8d6a499929946eeee0629b1574c868`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 17.3 KB (17311 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; 386

```console
$ docker pull julia@sha256:08851af22580d93edcff7af3400be7e451b3c74212780b4ccbab945dc0490f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301e3c68d9dab1a6c4102cc12904224ec14a689888175c58a3a0e74262374512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82545143988a5b43a1ac2b12be33d25c56903bb53a03c874f94074c56b82a9b2`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351580ccf1dcf1a05929fbb2822da43ba07255858a16167c7f816b5ebbc3bf3c`  
		Last Modified: Tue, 21 Oct 2025 21:50:05 GMT  
		Size: 237.6 MB (237589422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe17231b8108ee61fd58d12753ee11dec04c8c4e624108143ca7c284992c8de2`  
		Last Modified: Tue, 21 Oct 2025 01:19:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:7b9c5956245f1fea910d1714286310c78b6f9960efecdfb110461db882b01c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c96af9338b16a0e8ff0307467a6d0969dd848f75d42518d302919e0739305`

```dockerfile
```

-	Layers:
	-	`sha256:ca90562f0fd69376a215aaa90862d09081ee1ca8d926fd3bcaf4ba112ace9079`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58959592db46a248dc7122be1982bd94898c8b62ee559d96c9ae9a52185cc8c9`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 17.2 KB (17160 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; ppc64le

```console
$ docker pull julia@sha256:377c2602ad24e8f8df7425b947a50638aa20d4d2ff30ee7ab4f132be6a141e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41467295ab7ebac3684a2b2219084b17cd805ea7d5c331d7cf7b46812ea8906a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4f1de44718b36ed847bbbe4de338299d54a379fd71d6e6711dbb508570f510`  
		Last Modified: Tue, 21 Oct 2025 03:19:57 GMT  
		Size: 248.6 MB (248575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b937d93623990522216e1a0a83563425b4bb035cc4fa7ba6518c5ecc656d6`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:ddcd0937fb9cd450bb6dd81818867007e0222dfb2d12fafc3a1d44a0e412f67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17df2b6d907f57a694f30a0fd0f4b56c9cdb66360cee6ce262e2a3eaf5ba10`

```dockerfile
```

-	Layers:
	-	`sha256:efd875ebfd2967cbd9fd6c4bed7870805f9b888d456bcad1b571b1b3520936ac`  
		Last Modified: Tue, 21 Oct 2025 05:02:57 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d6c66e1cfab9ac54308f4f346503af7acd961b26f76c2142125061e2eb0573`  
		Last Modified: Tue, 21 Oct 2025 05:02:58 GMT  
		Size: 17.2 KB (17239 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:1a26e88a17bdfdb85336d88383e56217f386aa2458676363dcf66072d20ed1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506557781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe16003af3c162062c3b364cb4e0c9cfb350e841279e4aaeb8e65d76f7f6eab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:43:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:43:37 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:44:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f414e59fea2048693dfebf404f4ad0f980c980b1774cb29ae48cc293dd33cd`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9d16d2eefa04feecc234db6c45927164decd790dcdd12fb716ca2beaadb07`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85f34eaa04a9aa73ff9476f42d2ea1c1e0a81f2403fd0ab0a984c50143d1532`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372d9a32a2c3449d272982caa4939a2adaf2f9bce070d0fee80a4725299c6b0`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303deec3a031d89d2bd2b09857919b270db4130e539c4e69330fadc67f78f0c5`  
		Last Modified: Tue, 14 Oct 2025 23:03:58 GMT  
		Size: 286.1 MB (286070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f687bcae71dc1fe0ac3cd6c1aa42dcb4a88e4fce99d355839f214a46d5662ae3`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:1f3f5edaf659bb79ee9e91066a344f5b1796329dcd7601db9f44d9653c661cae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775034330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e10ce22e24661a2ecb8050770be373b4eefa519b740957ca350171909ddbee`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:59 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:43:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f81acf066b453e930a52b0f1cbd7f822cd50c543225d7d9cf6f16d51a27255`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cd4f5df3257e4533b67d0ccb0560ba0f1313540ceea39b1ceff9f2322981c`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c053e3eb854dea2a46d6194563ddf72979e2bccfda2c5c736035b0886ff4d`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6cb154dcd3209f47f3091b30e06342f360e4005b13509076d3436f421c3a5`  
		Last Modified: Tue, 14 Oct 2025 23:03:51 GMT  
		Size: 286.0 MB (286008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b2c48116adac832a87d095f7d2549732df53cc9dcce97fd0c11f83671dc97`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-bookworm`

```console
$ docker pull julia@sha256:1c0532da44349210e82ada44882147cbb75ff897b322aa3bacaa0f57319ba34e
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

### `julia:1.11.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:398039db5bcace9e4f649ca5c1f6d03710f1995695b132dc827201175e862fa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a193a1343cfc53434d6bd9fd5b67df4ea3baaa50c98ba98e454d0d1d2b302d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdacae64ad0ef312a8abbda8255aac0b873c406d849f5eba98857d3dddd20f28`  
		Last Modified: Tue, 21 Oct 2025 01:21:32 GMT  
		Size: 5.7 MB (5716297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56b41b941f9ddd8d84273ae5ad9b846f2a03a7fae1b459e59c6599fd5d5894`  
		Last Modified: Tue, 21 Oct 2025 14:10:27 GMT  
		Size: 288.8 MB (288788417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c01cbd534d4c3dd55640902025206b8896c0df6d9f44113850b9b2126f62ad`  
		Last Modified: Tue, 21 Oct 2025 01:21:31 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3650991c616122ed087a94a68308548aaff36007e55893b3aabfd6969b7107ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883afbac5f0beeca3142fefdb1ec3d0667285934a14297eb605f1557529505de`

```dockerfile
```

-	Layers:
	-	`sha256:6cc113a566ee9958f6f3cb8cc09cf9fdb24905b0159b9b90d7a384fe8ef67e05`  
		Last Modified: Tue, 21 Oct 2025 11:03:20 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2965f1a9014ae6d8430c59a6491f9dcd3378968fcfb3a913cd6d17737fdbab`  
		Last Modified: Tue, 21 Oct 2025 11:03:21 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:737aa5901a76684a1f4666e30afbb82c3227e746aebf299f0e305b504ecc1e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e572b897e07c49f1ec159d2b0f1c56e34b242aaca37d4b58a4b4c7981f9d8ac3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7d42b8b1a5aa2fe59b952ee689d785a46622ca0391174ce91c42d91899bc89`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 5.6 MB (5567093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8f62164c7192264de3339454f1c6c6a243f796044cc3474a89462f3b0be96`  
		Last Modified: Tue, 21 Oct 2025 13:40:24 GMT  
		Size: 304.6 MB (304646608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2f80538f06795371953bf234659723cb1c33d24b497e04b41859ff308f4e1b`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3ce21f54d92e8718caa367a8f5ddb0145c1da39c1a8a4cc7beed93cea5d189f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a4da0ffeb51f06d52085195f53b944fbac74d1554c37f4798a03991b5aa4e1`

```dockerfile
```

-	Layers:
	-	`sha256:a190f5f3f7baf0187988a461b52c46fb35a44a4d167bd80b4707219e80a6caf4`  
		Last Modified: Tue, 21 Oct 2025 08:02:47 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d546c395b1b0929bbb64c3e328421ab71127ae8b64a7dbcebb8c572fa162bf67`  
		Last Modified: Tue, 21 Oct 2025 08:02:48 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d1e478f72f6cc935fff064fe14e5bd0bf3e776b273539bc2d4d8f612cdc683f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff414cd59f151e142d5c053e97f892d63eb8a104a8381512588576e4cf9dc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a912b6853a709cb605792534a8ef346eb642e19cbf2604744511031a9a2e2313`  
		Last Modified: Tue, 21 Oct 2025 01:19:27 GMT  
		Size: 5.9 MB (5878012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ba8de8917734655b769288eeb6524c9c45e7806aba867500e1689cd7df68b`  
		Last Modified: Tue, 21 Oct 2025 02:55:45 GMT  
		Size: 237.6 MB (237555799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae7fd496f776220d47329c8602768c58a5c87ef69e0881d70fcbd0cd563fae7`  
		Last Modified: Tue, 21 Oct 2025 01:19:27 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:34b0241daf94d698a79d88f4e4e797e1ac314a7b706a1000569356eb19fbdcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6beb3a9c8569c651cf07d8a62e48aa7b53746207728b7afd8f70d6aadc233a`

```dockerfile
```

-	Layers:
	-	`sha256:f9fc4ad5c7c17855ef666449ae6824c46c5952f454996fb8c6701a15d902babd`  
		Last Modified: Tue, 21 Oct 2025 11:03:28 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839790cb167df012aea9492c6fc9cf41e1c009fccbe560874552b6b04c7e7798`  
		Last Modified: Tue, 21 Oct 2025 11:03:29 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:9d83aae3c9991b3b389f9f1619a6fd0a3c3c3cb95458a1fb44d35e7e9e693eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aed8a4b359c462a5e9ca88c84c5ce2500ae1af93ece83e82cfe0d9ac806fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc155374c7db12d97ec8dfc57f566dd402662f9a5876305b298bced2fb30309b`  
		Last Modified: Tue, 21 Oct 2025 01:46:55 GMT  
		Size: 6.3 MB (6256276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483cbf9a6fcd9f801cefe9174ac90d0c3273a5cedbed0d5eebab73acf38e6ef8`  
		Last Modified: Tue, 21 Oct 2025 01:46:49 GMT  
		Size: 248.6 MB (248553870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8adfaf14441b4b616dee5f105ce1ee2405f230ab9656420573232387a87301`  
		Last Modified: Tue, 21 Oct 2025 01:46:54 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:92ee77a70b5f5f83f876488fba8a581b470d7d6bc17058ca4b81434e937471a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27822b8ba478a2ba49d504824a1a9c6dfe020fc21bb6700e76cc514f222f09f7`

```dockerfile
```

-	Layers:
	-	`sha256:e2e5f0499d02236fa1a7e5da9b344f97ff0403082333a6d2b351c89f82ffbc0b`  
		Last Modified: Tue, 21 Oct 2025 05:03:02 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f262c2e27264305d1c1eada818f6f98cf9d1bee310fe288e848f695d3a11d38`  
		Last Modified: Tue, 21 Oct 2025 05:03:03 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-trixie`

```console
$ docker pull julia@sha256:520a0e46bd2574ba4d96e4fd6e5ecde251f2258645730566ba1d6da4faa8c3ff
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

### `julia:1.11.7-trixie` - linux; amd64

```console
$ docker pull julia@sha256:c1a4b7d7f398db0f3689848c5d5d4830aaaf5b028aa8a2d22636a78caf6a28b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c050b786f30db3e872c49ef9e199a3f8e998c1d376d7489b833672fb43a1992c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f197fd3303ab25f3f09540cc089e3f5efc0d2c3da24f72515e1ef2120013e3f`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 6.2 MB (6242779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd2d9030da9c64039ed492740b7e2d81ef2293cb1d32ccc1e95fd3040adc2e7`  
		Last Modified: Tue, 21 Oct 2025 11:08:58 GMT  
		Size: 288.8 MB (288825612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4693ebdb3345b02a5895e8ce2151682eb3f2ce609c793798769903f3c49d0`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1e39a89eaaa73274a6235ddaf1ea96fafcff9d95d94f7ee271383de31c2e941a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd953062c4bf43dba26149d26978e48666f70f3a2b391f828f00c936ba07468d`

```dockerfile
```

-	Layers:
	-	`sha256:8bb944154d3357a7cfd615409baa93815f6df29df973ef0a4f61b14e20ec7b51`  
		Last Modified: Tue, 21 Oct 2025 11:03:13 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7c2157a84659528c287b0c20d002b412df2944c6f26949ca459730287a5fe0a`  
		Last Modified: Tue, 21 Oct 2025 11:03:14 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:28a6633dde0f2f68ef34736e32d02465e7d8fc358a85a93aab0d4dc1a47d1f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc88ee5486f116ff82337aa3d80476c96f998f9595d724cc3b796946ef0fd4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7317e038a5aee60731ca3e760aa1c072354ae7d86ead1c4a3e12e9868f7ce90`  
		Last Modified: Tue, 21 Oct 2025 01:20:40 GMT  
		Size: 6.2 MB (6153023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd99a31f1a641fb61386055fbb8250f82030ee4c2e3412c994d2eacffdeb3b3`  
		Last Modified: Tue, 21 Oct 2025 11:29:01 GMT  
		Size: 304.7 MB (304672756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e973a1c1d9ab3b9d844abfd958960f0a9c4ed26a5c600b14d016adf4aa40a2`  
		Last Modified: Tue, 21 Oct 2025 01:20:39 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2356356811d039bbbbdda5867ba0b5c0e7e385c3385e20c223d9c7f4a64207d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eddab6c164ab8e6448636761f0d405cc20b2ddb207abd5d2bb5b547bf8b2536`

```dockerfile
```

-	Layers:
	-	`sha256:fc73fc6e0e142e936163c7d3d63c5e4a834fb75a9c39ad3783608321478d2116`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63968c49ec46ef1596ec92911d27817eeb8d6a499929946eeee0629b1574c868`  
		Last Modified: Tue, 21 Oct 2025 11:03:18 GMT  
		Size: 17.3 KB (17311 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; 386

```console
$ docker pull julia@sha256:08851af22580d93edcff7af3400be7e451b3c74212780b4ccbab945dc0490f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301e3c68d9dab1a6c4102cc12904224ec14a689888175c58a3a0e74262374512`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82545143988a5b43a1ac2b12be33d25c56903bb53a03c874f94074c56b82a9b2`  
		Last Modified: Tue, 21 Oct 2025 01:19:23 GMT  
		Size: 6.4 MB (6427717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351580ccf1dcf1a05929fbb2822da43ba07255858a16167c7f816b5ebbc3bf3c`  
		Last Modified: Tue, 21 Oct 2025 21:50:05 GMT  
		Size: 237.6 MB (237589422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe17231b8108ee61fd58d12753ee11dec04c8c4e624108143ca7c284992c8de2`  
		Last Modified: Tue, 21 Oct 2025 01:19:22 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7b9c5956245f1fea910d1714286310c78b6f9960efecdfb110461db882b01c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243c96af9338b16a0e8ff0307467a6d0969dd848f75d42518d302919e0739305`

```dockerfile
```

-	Layers:
	-	`sha256:ca90562f0fd69376a215aaa90862d09081ee1ca8d926fd3bcaf4ba112ace9079`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58959592db46a248dc7122be1982bd94898c8b62ee559d96c9ae9a52185cc8c9`  
		Last Modified: Tue, 21 Oct 2025 11:03:22 GMT  
		Size: 17.2 KB (17160 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:377c2602ad24e8f8df7425b947a50638aa20d4d2ff30ee7ab4f132be6a141e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41467295ab7ebac3684a2b2219084b17cd805ea7d5c331d7cf7b46812ea8906a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 16 Sep 2025 05:59:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 16 Sep 2025 05:59:21 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 05:59:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Sep 2025 05:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Sep 2025 05:59:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1de2b27460e6eaedecd0fac78f7602b81ad331d709229d5e0a1fd14c6f5f3e`  
		Last Modified: Tue, 21 Oct 2025 01:44:24 GMT  
		Size: 6.7 MB (6682232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4f1de44718b36ed847bbbe4de338299d54a379fd71d6e6711dbb508570f510`  
		Last Modified: Tue, 21 Oct 2025 03:19:57 GMT  
		Size: 248.6 MB (248575956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b937d93623990522216e1a0a83563425b4bb035cc4fa7ba6518c5ecc656d6`  
		Last Modified: Tue, 21 Oct 2025 01:44:19 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ddcd0937fb9cd450bb6dd81818867007e0222dfb2d12fafc3a1d44a0e412f67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc17df2b6d907f57a694f30a0fd0f4b56c9cdb66360cee6ce262e2a3eaf5ba10`

```dockerfile
```

-	Layers:
	-	`sha256:efd875ebfd2967cbd9fd6c4bed7870805f9b888d456bcad1b571b1b3520936ac`  
		Last Modified: Tue, 21 Oct 2025 05:02:57 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d6c66e1cfab9ac54308f4f346503af7acd961b26f76c2142125061e2eb0573`  
		Last Modified: Tue, 21 Oct 2025 05:02:58 GMT  
		Size: 17.2 KB (17239 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-windowsservercore`

```console
$ docker pull julia@sha256:d9cfd001c2470fe693f01e5cf111d84115fd23409931fa881e9fd54ed7581286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.11.7-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:1a26e88a17bdfdb85336d88383e56217f386aa2458676363dcf66072d20ed1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506557781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe16003af3c162062c3b364cb4e0c9cfb350e841279e4aaeb8e65d76f7f6eab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:43:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:43:37 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:44:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f414e59fea2048693dfebf404f4ad0f980c980b1774cb29ae48cc293dd33cd`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9d16d2eefa04feecc234db6c45927164decd790dcdd12fb716ca2beaadb07`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85f34eaa04a9aa73ff9476f42d2ea1c1e0a81f2403fd0ab0a984c50143d1532`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372d9a32a2c3449d272982caa4939a2adaf2f9bce070d0fee80a4725299c6b0`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303deec3a031d89d2bd2b09857919b270db4130e539c4e69330fadc67f78f0c5`  
		Last Modified: Tue, 14 Oct 2025 23:03:58 GMT  
		Size: 286.1 MB (286070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f687bcae71dc1fe0ac3cd6c1aa42dcb4a88e4fce99d355839f214a46d5662ae3`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:1f3f5edaf659bb79ee9e91066a344f5b1796329dcd7601db9f44d9653c661cae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775034330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e10ce22e24661a2ecb8050770be373b4eefa519b740957ca350171909ddbee`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:59 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:43:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f81acf066b453e930a52b0f1cbd7f822cd50c543225d7d9cf6f16d51a27255`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cd4f5df3257e4533b67d0ccb0560ba0f1313540ceea39b1ceff9f2322981c`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c053e3eb854dea2a46d6194563ddf72979e2bccfda2c5c736035b0886ff4d`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6cb154dcd3209f47f3091b30e06342f360e4005b13509076d3436f421c3a5`  
		Last Modified: Tue, 14 Oct 2025 23:03:51 GMT  
		Size: 286.0 MB (286008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b2c48116adac832a87d095f7d2549732df53cc9dcce97fd0c11f83671dc97`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:776b1833a5b24002caee933bc1b5e86569c94efdb02be89e80a09c76080c8bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1.11.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:1f3f5edaf659bb79ee9e91066a344f5b1796329dcd7601db9f44d9653c661cae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1775034330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e10ce22e24661a2ecb8050770be373b4eefa519b740957ca350171909ddbee`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:41:59 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:42:00 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:43:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:43:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f81acf066b453e930a52b0f1cbd7f822cd50c543225d7d9cf6f16d51a27255`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381cd4f5df3257e4533b67d0ccb0560ba0f1313540ceea39b1ceff9f2322981c`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c053e3eb854dea2a46d6194563ddf72979e2bccfda2c5c736035b0886ff4d`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c6cb154dcd3209f47f3091b30e06342f360e4005b13509076d3436f421c3a5`  
		Last Modified: Tue, 14 Oct 2025 23:03:51 GMT  
		Size: 286.0 MB (286008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b2c48116adac832a87d095f7d2549732df53cc9dcce97fd0c11f83671dc97`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:e904e07585d5ea8cc8c94a69eee35d81a0083b58a974feec1a81ebaaf6f69abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1.11.7-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:1a26e88a17bdfdb85336d88383e56217f386aa2458676363dcf66072d20ed1a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506557781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe16003af3c162062c3b364cb4e0c9cfb350e841279e4aaeb8e65d76f7f6eab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:43:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 14 Oct 2025 20:43:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 14 Oct 2025 20:43:37 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 14 Oct 2025 20:44:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:44:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f414e59fea2048693dfebf404f4ad0f980c980b1774cb29ae48cc293dd33cd`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee9d16d2eefa04feecc234db6c45927164decd790dcdd12fb716ca2beaadb07`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85f34eaa04a9aa73ff9476f42d2ea1c1e0a81f2403fd0ab0a984c50143d1532`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f372d9a32a2c3449d272982caa4939a2adaf2f9bce070d0fee80a4725299c6b0`  
		Last Modified: Tue, 14 Oct 2025 20:52:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303deec3a031d89d2bd2b09857919b270db4130e539c4e69330fadc67f78f0c5`  
		Last Modified: Tue, 14 Oct 2025 23:03:58 GMT  
		Size: 286.1 MB (286070702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f687bcae71dc1fe0ac3cd6c1aa42dcb4a88e4fce99d355839f214a46d5662ae3`  
		Last Modified: Tue, 14 Oct 2025 20:52:47 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12`

```console
$ docker pull julia@sha256:6df3a44f17932272ac3524a39c554bf942a49902da0ed8f58f70beb03cf0b691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.12` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-bookworm`

```console
$ docker pull julia@sha256:f769ef90b49807694da53abb2ca8c6c67532b9e64d7b7bb5571f76d5ff477fcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:1aa85df6ec49583176b3d63173ff7a2c4e9331ae0b9f972855300f7c42f87ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df569a38312c003e97032a8400079825dee34a9312690f12cac8da07192240cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230bd169a62bdd742f5fe1526024758c9182734b2090afb36f7e9b11e1d56c1f`  
		Last Modified: Tue, 21 Oct 2025 20:15:41 GMT  
		Size: 5.7 MB (5716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b94ddc353e5019807ab431f31f99fde76c06428fd4cf7e028e597d04a5740`  
		Last Modified: Wed, 22 Oct 2025 01:18:52 GMT  
		Size: 289.5 MB (289470982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f404cac60bf373235bd1c33e9eeb8a524d328181898fbcffc99312339216d02`  
		Last Modified: Tue, 21 Oct 2025 20:15:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c44d1a92f620cbf4341c7925e7df60c230efd111d753fd591bfd8ec514038e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e1512307c7da2bd465c639735be18e024d648fa0b91349b19b9d380be9df86`

```dockerfile
```

-	Layers:
	-	`sha256:584b20012bf0215b3e38226088d4e60467593cb18f440178131d34325a173ce7`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f32c356b06f4210b222c36b6e0d30b546d1eb64c6ac6bd3881a552b91de57ec`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:db7e63bcfaec71ea6e4281b4e92d081a1764b56cc6a9ff17cc15962b840cbd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcebdb683edeca155ae87ab12b238118291e7afeef30cd4d65bbb47dc57b98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5291731e8c0d3673a1a88ec62c3b52a25f60c6b223611669ff46969390581`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 5.6 MB (5567174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9c6938264fafd3aec09c37207ec05ed10474b77334515ecc4ec31d88bf5e1`  
		Last Modified: Tue, 21 Oct 2025 22:31:49 GMT  
		Size: 310.2 MB (310205330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974b20ce9e4f47cf1dc904cdd42abc7dd5ce1273805b63d020904d9e5676047`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:080e22faa91f324fdc0b3bcab563ac06d536a855ad787d9507c6a08a2b6fbfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdc62b09c5f7605ac15c3b7dbe4873246cfb7b61cb2406bc84e816b58de00c5`

```dockerfile
```

-	Layers:
	-	`sha256:12f1b6fb81092bc32c3ec2e038592a894653eefde55b19513b91d9b1cd84b882`  
		Last Modified: Tue, 21 Oct 2025 20:02:36 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a91fb3011ec1aeadac1477bea3e37c91e22e3dec83e151e44348b9c88428366`  
		Last Modified: Tue, 21 Oct 2025 20:02:37 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d5f8bf506eac97acd36cb2b8f406a27119d33b7f4dd0f25fd5ba83e45f67cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dcff817f5a853949791b9226becba3a5c8264b8251fcc8c8a347ae0ecb3c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac3a9ad9b8eabd3b5d50f72eebebfa697cdbb06c950c34087e6289736881bb0`  
		Last Modified: Tue, 21 Oct 2025 18:17:26 GMT  
		Size: 5.9 MB (5878048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04cdd9874dc106b265e5ba8b55d1e1d1c26603f7682c64f4365b76322b55d54`  
		Last Modified: Tue, 21 Oct 2025 22:31:16 GMT  
		Size: 231.0 MB (231003075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55c53a4a537b4baf40d7dd1a9782baf04a5bcd8647966a03bb1bbcabadb072`  
		Last Modified: Tue, 21 Oct 2025 18:17:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c34b15651101f3a14a8601b87b38e9dee4442fb327c129b770ac5fb1e5b1381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1b43567d7d2e8ebbaf9036174313b13740f20b7df0f50acbf80d2e87bcdb5d`

```dockerfile
```

-	Layers:
	-	`sha256:cddd1c3c366ee6a4f085600d7a1893078914ecdb31df262b989de8065683e47a`  
		Last Modified: Tue, 21 Oct 2025 20:02:41 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba22b294c989c47dcd755204201d14d2141f0e24bba2f0b2f23e9e827d7a59c0`  
		Last Modified: Tue, 21 Oct 2025 20:02:42 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-trixie`

```console
$ docker pull julia@sha256:0d11d89a94c97c35ba7f1acc8e77287b47dbd69a24e078b210d11c21f69ea7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12-trixie` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-windowsservercore`

```console
$ docker pull julia@sha256:dde8fbb99f3a8cc20ff9248560e471f28794406993756d349d0ca67839562ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.12-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:da76ee4b1c8838bf073c4463082881c9edbed92a046d4d9f3ec7a3785fbd37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3f33be8fe9e3496a9e954d3af5f3466caf3201d9c8c009df451489829551d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1.12-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1`

```console
$ docker pull julia@sha256:6df3a44f17932272ac3524a39c554bf942a49902da0ed8f58f70beb03cf0b691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.12.1` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.1` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-bookworm`

```console
$ docker pull julia@sha256:f769ef90b49807694da53abb2ca8c6c67532b9e64d7b7bb5571f76d5ff477fcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:1aa85df6ec49583176b3d63173ff7a2c4e9331ae0b9f972855300f7c42f87ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df569a38312c003e97032a8400079825dee34a9312690f12cac8da07192240cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230bd169a62bdd742f5fe1526024758c9182734b2090afb36f7e9b11e1d56c1f`  
		Last Modified: Tue, 21 Oct 2025 20:15:41 GMT  
		Size: 5.7 MB (5716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b94ddc353e5019807ab431f31f99fde76c06428fd4cf7e028e597d04a5740`  
		Last Modified: Wed, 22 Oct 2025 01:18:52 GMT  
		Size: 289.5 MB (289470982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f404cac60bf373235bd1c33e9eeb8a524d328181898fbcffc99312339216d02`  
		Last Modified: Tue, 21 Oct 2025 20:15:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c44d1a92f620cbf4341c7925e7df60c230efd111d753fd591bfd8ec514038e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e1512307c7da2bd465c639735be18e024d648fa0b91349b19b9d380be9df86`

```dockerfile
```

-	Layers:
	-	`sha256:584b20012bf0215b3e38226088d4e60467593cb18f440178131d34325a173ce7`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f32c356b06f4210b222c36b6e0d30b546d1eb64c6ac6bd3881a552b91de57ec`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:db7e63bcfaec71ea6e4281b4e92d081a1764b56cc6a9ff17cc15962b840cbd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcebdb683edeca155ae87ab12b238118291e7afeef30cd4d65bbb47dc57b98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5291731e8c0d3673a1a88ec62c3b52a25f60c6b223611669ff46969390581`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 5.6 MB (5567174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9c6938264fafd3aec09c37207ec05ed10474b77334515ecc4ec31d88bf5e1`  
		Last Modified: Tue, 21 Oct 2025 22:31:49 GMT  
		Size: 310.2 MB (310205330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974b20ce9e4f47cf1dc904cdd42abc7dd5ce1273805b63d020904d9e5676047`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:080e22faa91f324fdc0b3bcab563ac06d536a855ad787d9507c6a08a2b6fbfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdc62b09c5f7605ac15c3b7dbe4873246cfb7b61cb2406bc84e816b58de00c5`

```dockerfile
```

-	Layers:
	-	`sha256:12f1b6fb81092bc32c3ec2e038592a894653eefde55b19513b91d9b1cd84b882`  
		Last Modified: Tue, 21 Oct 2025 20:02:36 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a91fb3011ec1aeadac1477bea3e37c91e22e3dec83e151e44348b9c88428366`  
		Last Modified: Tue, 21 Oct 2025 20:02:37 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d5f8bf506eac97acd36cb2b8f406a27119d33b7f4dd0f25fd5ba83e45f67cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dcff817f5a853949791b9226becba3a5c8264b8251fcc8c8a347ae0ecb3c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac3a9ad9b8eabd3b5d50f72eebebfa697cdbb06c950c34087e6289736881bb0`  
		Last Modified: Tue, 21 Oct 2025 18:17:26 GMT  
		Size: 5.9 MB (5878048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04cdd9874dc106b265e5ba8b55d1e1d1c26603f7682c64f4365b76322b55d54`  
		Last Modified: Tue, 21 Oct 2025 22:31:16 GMT  
		Size: 231.0 MB (231003075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55c53a4a537b4baf40d7dd1a9782baf04a5bcd8647966a03bb1bbcabadb072`  
		Last Modified: Tue, 21 Oct 2025 18:17:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c34b15651101f3a14a8601b87b38e9dee4442fb327c129b770ac5fb1e5b1381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1b43567d7d2e8ebbaf9036174313b13740f20b7df0f50acbf80d2e87bcdb5d`

```dockerfile
```

-	Layers:
	-	`sha256:cddd1c3c366ee6a4f085600d7a1893078914ecdb31df262b989de8065683e47a`  
		Last Modified: Tue, 21 Oct 2025 20:02:41 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba22b294c989c47dcd755204201d14d2141f0e24bba2f0b2f23e9e827d7a59c0`  
		Last Modified: Tue, 21 Oct 2025 20:02:42 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.1-trixie`

```console
$ docker pull julia@sha256:0d11d89a94c97c35ba7f1acc8e77287b47dbd69a24e078b210d11c21f69ea7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-trixie` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.1-windowsservercore`

```console
$ docker pull julia@sha256:dde8fbb99f3a8cc20ff9248560e471f28794406993756d349d0ca67839562ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:1.12.1-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.1-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:da76ee4b1c8838bf073c4463082881c9edbed92a046d4d9f3ec7a3785fbd37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:1.12.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3f33be8fe9e3496a9e954d3af5f3466caf3201d9c8c009df451489829551d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:1.12.1-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:f769ef90b49807694da53abb2ca8c6c67532b9e64d7b7bb5571f76d5ff477fcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:1aa85df6ec49583176b3d63173ff7a2c4e9331ae0b9f972855300f7c42f87ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df569a38312c003e97032a8400079825dee34a9312690f12cac8da07192240cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230bd169a62bdd742f5fe1526024758c9182734b2090afb36f7e9b11e1d56c1f`  
		Last Modified: Tue, 21 Oct 2025 20:15:41 GMT  
		Size: 5.7 MB (5716354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b94ddc353e5019807ab431f31f99fde76c06428fd4cf7e028e597d04a5740`  
		Last Modified: Wed, 22 Oct 2025 01:18:52 GMT  
		Size: 289.5 MB (289470982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f404cac60bf373235bd1c33e9eeb8a524d328181898fbcffc99312339216d02`  
		Last Modified: Tue, 21 Oct 2025 20:15:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c44d1a92f620cbf4341c7925e7df60c230efd111d753fd591bfd8ec514038e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e1512307c7da2bd465c639735be18e024d648fa0b91349b19b9d380be9df86`

```dockerfile
```

-	Layers:
	-	`sha256:584b20012bf0215b3e38226088d4e60467593cb18f440178131d34325a173ce7`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f32c356b06f4210b222c36b6e0d30b546d1eb64c6ac6bd3881a552b91de57ec`  
		Last Modified: Tue, 21 Oct 2025 23:02:22 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:db7e63bcfaec71ea6e4281b4e92d081a1764b56cc6a9ff17cc15962b840cbd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcebdb683edeca155ae87ab12b238118291e7afeef30cd4d65bbb47dc57b98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5291731e8c0d3673a1a88ec62c3b52a25f60c6b223611669ff46969390581`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 5.6 MB (5567174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f9c6938264fafd3aec09c37207ec05ed10474b77334515ecc4ec31d88bf5e1`  
		Last Modified: Tue, 21 Oct 2025 22:31:49 GMT  
		Size: 310.2 MB (310205330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8974b20ce9e4f47cf1dc904cdd42abc7dd5ce1273805b63d020904d9e5676047`  
		Last Modified: Tue, 21 Oct 2025 18:16:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:080e22faa91f324fdc0b3bcab563ac06d536a855ad787d9507c6a08a2b6fbfb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdc62b09c5f7605ac15c3b7dbe4873246cfb7b61cb2406bc84e816b58de00c5`

```dockerfile
```

-	Layers:
	-	`sha256:12f1b6fb81092bc32c3ec2e038592a894653eefde55b19513b91d9b1cd84b882`  
		Last Modified: Tue, 21 Oct 2025 20:02:36 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a91fb3011ec1aeadac1477bea3e37c91e22e3dec83e151e44348b9c88428366`  
		Last Modified: Tue, 21 Oct 2025 20:02:37 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:d5f8bf506eac97acd36cb2b8f406a27119d33b7f4dd0f25fd5ba83e45f67cbdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86dcff817f5a853949791b9226becba3a5c8264b8251fcc8c8a347ae0ecb3c8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac3a9ad9b8eabd3b5d50f72eebebfa697cdbb06c950c34087e6289736881bb0`  
		Last Modified: Tue, 21 Oct 2025 18:17:26 GMT  
		Size: 5.9 MB (5878048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04cdd9874dc106b265e5ba8b55d1e1d1c26603f7682c64f4365b76322b55d54`  
		Last Modified: Tue, 21 Oct 2025 22:31:16 GMT  
		Size: 231.0 MB (231003075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db55c53a4a537b4baf40d7dd1a9782baf04a5bcd8647966a03bb1bbcabadb072`  
		Last Modified: Tue, 21 Oct 2025 18:17:25 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:c34b15651101f3a14a8601b87b38e9dee4442fb327c129b770ac5fb1e5b1381f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1b43567d7d2e8ebbaf9036174313b13740f20b7df0f50acbf80d2e87bcdb5d`

```dockerfile
```

-	Layers:
	-	`sha256:cddd1c3c366ee6a4f085600d7a1893078914ecdb31df262b989de8065683e47a`  
		Last Modified: Tue, 21 Oct 2025 20:02:41 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba22b294c989c47dcd755204201d14d2141f0e24bba2f0b2f23e9e827d7a59c0`  
		Last Modified: Tue, 21 Oct 2025 20:02:42 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:6df3a44f17932272ac3524a39c554bf942a49902da0ed8f58f70beb03cf0b691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:trixie`

```console
$ docker pull julia@sha256:0d11d89a94c97c35ba7f1acc8e77287b47dbd69a24e078b210d11c21f69ea7dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:trixie` - linux; amd64

```console
$ docker pull julia@sha256:100a16e7795fe132b16f6d276c5d55a9b9e9b663ef74534d9f1e77e116cb6616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8288ace8a3f30304d5f5f6cfe7d0ce2200a3be251f5ad78b2240d3b2c421c9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cb54a235ac43c57eac877411d6355c41017d5faef37fde2eb768aa00781efb`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 6.2 MB (6242815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0dd40c781b44127c5eaafbb88fd7a1dc82e5914ed7feafa9c3e3450977a71`  
		Last Modified: Tue, 21 Oct 2025 23:03:12 GMT  
		Size: 289.5 MB (289509752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8184e382675284be5b296eedf07655a48e9e4edf5c410d2fc5d02957a1f6f`  
		Last Modified: Tue, 21 Oct 2025 20:14:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7108d157010090f6c301b858906e7ab22f23a359349fb21a0461a7539c8173b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e03255e51f7d62fc8470a4f2ac323c216a74e10df7e3535113bdf885be9c0af`

```dockerfile
```

-	Layers:
	-	`sha256:f0d77c3c948134d3fd7b17e391096b10a5f4e18c99b8199740e998bda7315914`  
		Last Modified: Tue, 21 Oct 2025 23:02:17 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5bdf79615d1bf8502b1acf50226bc4edc3b6b948933d6eb8e91a0659bd5d80`  
		Last Modified: Tue, 21 Oct 2025 23:02:18 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:51d8357e427dad5e9664ec71f22cb0bb92f051207ce5e52f6f2212b919ff1a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a388e5c76234c765df9be5ee6dab9786d1692abc23d7de21e7fd7bfed3a09537`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9cd5ffd680616fec199e43e07c69ffc88c2b0852eb7f918d616adc3140dec`  
		Last Modified: Tue, 21 Oct 2025 18:16:23 GMT  
		Size: 6.2 MB (6153056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb3f146333de7f6b9351b4b2301d9e47acec5cc50866e27c948c0542a960d105`  
		Last Modified: Tue, 21 Oct 2025 22:34:41 GMT  
		Size: 310.2 MB (310243585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5d1ba56190d917d38b12f38c22e2b05ffd4db08582102d22b0cbae187c9a1`  
		Last Modified: Tue, 21 Oct 2025 18:16:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:6c5bace6b0ee197421606a5b21ee216f04ab2cc1e8a34481019f021cb9756f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3740e8034facf342b8cd0d1d019e62ae5ec6ad7b7f19af288ca461beca83bc0e`

```dockerfile
```

-	Layers:
	-	`sha256:259cc1f36a4b91356421af6402bf017844606f27b2f8740b4033bb370cd819e0`  
		Last Modified: Tue, 21 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff67604e4a9232b4d114b4582b87f778a3c9d05cf0968f2a7d1da0df524bb7ea`  
		Last Modified: Tue, 21 Oct 2025 20:02:28 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:9b218ed258b8d54a63292566fdb4b3fb9500bb8f488f3823eb16fb1fbb8e1326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643168051df497002232e3c36e6863975d0bc4f4a4684f0da5effd804d0eabbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Sat, 18 Oct 2025 05:59:24 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 18 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Sat, 18 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.1
# Sat, 18 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 18 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 18 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee2226dfddcc86e89e175e51f92adbe160691f1050abb8b9a84c837c0d8ac6e`  
		Last Modified: Tue, 21 Oct 2025 18:17:16 GMT  
		Size: 6.4 MB (6427772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93dcadcb45a78c0e624ef20df5fd71215a81db5ade8f7332e8fa9a217896bb2`  
		Last Modified: Tue, 21 Oct 2025 22:34:30 GMT  
		Size: 231.0 MB (231034237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f938d913ca31948e13e6a2d685fb3d6856737372b93805567106c6e8b0f450`  
		Last Modified: Tue, 21 Oct 2025 18:17:15 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a4641c1e22d06855f3c86435f1afd4576b3c5ab8ed2a5097c952463e2b29f80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abf3ae68a676abdd1bc2fd91f0a87fb5d9be17345ba3225160b43b1324a12bc`

```dockerfile
```

-	Layers:
	-	`sha256:82c177774996f99c945f5a339402dca10f4f0ecf3ac85c03e722873bc3e3d5fd`  
		Last Modified: Tue, 21 Oct 2025 20:02:32 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc02343c4dbfd7d1a597c2d8bfdb06d5f059f071cc6cb30208a3ea21406adad`  
		Last Modified: Tue, 21 Oct 2025 20:02:34 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:dde8fbb99f3a8cc20ff9248560e471f28794406993756d349d0ca67839562ddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `julia:windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:da76ee4b1c8838bf073c4463082881c9edbed92a046d4d9f3ec7a3785fbd37ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull julia@sha256:31cccda2394790eab545bf48cd20fb6a228d433e9448cfea4a49091665525c84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1873787233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7c82b42c4d806b7b890d248170501dd5b6623d2c8ffc94c6b8546974cb1cc6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 21 Oct 2025 18:14:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:06 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1599542500940c0b4e37228fa8a09ae85358f30d28f350aeddfa47b9bad90138`  
		Last Modified: Tue, 21 Oct 2025 18:28:32 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a416b9354a50171f26c969fe5aad7807a4103d0a3fa128527cedcf8470cb644`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66afcc165890543dc94f25be03156b98295f6277896f17745528a9564aaf3590`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261d0705096cb581c61d78fcc9408c8f19ee8a102532ee0f9c58119a67d25d86`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781eb96e56ba4ed9bca6fb38a880b4917c25a649afa6c9b14eae34c868956f7d`  
		Last Modified: Tue, 21 Oct 2025 20:02:58 GMT  
		Size: 384.8 MB (384761535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3f7bae950b3cc91bc0d54aecae2e59ea30d0139009dd21985a08ce0bd2a972`  
		Last Modified: Tue, 21 Oct 2025 18:37:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:3f33be8fe9e3496a9e954d3af5f3466caf3201d9c8c009df451489829551d87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull julia@sha256:c74b7617ea08c37192fdd7564fbff32a861a674eeecbc858a6deea20f141dfdd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605242426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b91d0bd0826e37122a7b8da19df1d1b1924ecf4d0447148eef2ccef3b9085c4`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 21 Oct 2025 18:14:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Oct 2025 18:33:58 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 21 Oct 2025 18:34:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 21 Oct 2025 18:34:01 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 21 Oct 2025 18:35:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 21 Oct 2025 18:35:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365f67b52bd476e2c905e369b1aabcc60e8cb7a2ea77d6a39d21ccae187fd67d`  
		Last Modified: Tue, 21 Oct 2025 18:33:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f169df685cce7438afab616c1b275448de2ac62e047c1cb1daaea8b5e38053`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b37f5735eb1bedb8eb641466c37a6c51388ff97309c1a4b4b9efccde6f955f`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f628f979df85986cf1d3f7915fe75a316791af45d825a203c52cd05e0b6d97`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c671b3cd84fd07d7d456b5939b8af5b65afa3e3634a19c718752c8229e1221a2`  
		Last Modified: Tue, 21 Oct 2025 20:04:11 GMT  
		Size: 384.8 MB (384755470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd07251fcad21a805007e8e1af5a090b6b9af343c88495acde62853807062320`  
		Last Modified: Tue, 21 Oct 2025 18:36:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
