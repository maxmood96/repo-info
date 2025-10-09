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
-	[`julia:1.12.0`](#julia1120)
-	[`julia:1.12.0-bookworm`](#julia1120-bookworm)
-	[`julia:1.12.0-trixie`](#julia1120-trixie)
-	[`julia:1.12.0-windowsservercore`](#julia1120-windowsservercore)
-	[`julia:1.12.0-windowsservercore-ltsc2022`](#julia1120-windowsservercore-ltsc2022)
-	[`julia:1.12.0-windowsservercore-ltsc2025`](#julia1120-windowsservercore-ltsc2025)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:latest`](#julialatest)
-	[`julia:trixie`](#juliatrixie)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)
-	[`julia:windowsservercore-ltsc2025`](#juliawindowsservercore-ltsc2025)

## `julia:1`

```console
$ docker pull julia@sha256:d5d792f8fedb069a90527a3d632ce4510a90c32411d8a72fdf0d1935ee6df9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:99ddf36d97eaa12ca9e43d81d9d70025aa280ecd3d45b0e1f94d291d2bbe3782
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
$ docker pull julia@sha256:70230d2c81d4ab3554a0334bda465610d9cce461111fa141d144a2148114c22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319506830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903d66d0bffa44a76611abe66dea2fe89cd25b87fe95e848fd8de7a9c3a867f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca811ac4307c1488b6cbd2dc62d7c1c078ca5a4cacf34e3ffc9b29c7b4ef751c`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 5.7 MB (5716323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b508acb0220a8b7f26c2acc53b6c3a0fd53c4a00d2f877eac41e1e3fcd90d`  
		Last Modified: Wed, 08 Oct 2025 20:16:45 GMT  
		Size: 285.6 MB (285561802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f204c56b62295f834ff92a332d566df85fd81d75c9a4fde2c77580e6adde2d18`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a4b333091e24508599a8b4a6030f4ad8262038f98c1df050e1d3c100674bd76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668e975d30b0146d868bbcca6f61460b2089b6663dff4d82904e438215e4d962`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9ea196137e278ca2a0f42bb7af728b85cdabd4935748d40835e893ef0bf6a`  
		Last Modified: Wed, 08 Oct 2025 23:02:39 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a306454b16d0438c2a002d23e1c75044bb30b3b373e0dbed643c477681e686`  
		Last Modified: Wed, 08 Oct 2025 23:02:40 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d7d84080e9e6b24a1769bf0a011b69cfb724c6dbf0108c5aad4cadeab63fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339278659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a275f979d0c3cbaaf31b3da876e643e4ab62a1ac8ece3ae4df2392d0961efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f4ce1b9a56f84c283da7334e6218a33edfd2259168bc23fd77e9ea9b3f268`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 5.6 MB (5567102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2848785684a344ab32295e4c355472ff20a0be6c4b7f566098935a7361de73`  
		Last Modified: Wed, 08 Oct 2025 20:16:54 GMT  
		Size: 305.6 MB (305609040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11b9d3dca8c47b9cfcf2e28410520354f664aba6d18d1444c83a385940bd15e`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f1e1e094704c4b93414f41628e6a955518a9aeb7dbe51cfc74199d372e088637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66118456964de660d6987e1ebbe49fb01de41efa91d6f3d755086418d8ce952`

```dockerfile
```

-	Layers:
	-	`sha256:84eb79e0de87050b0a5e9c40fffbeda7996d073878db251c2e746a40a64e227a`  
		Last Modified: Wed, 08 Oct 2025 23:02:44 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6e711a3ba83235e573cf41124ee406a2abd99d3a3970225c8aec65286d0f09`  
		Last Modified: Wed, 08 Oct 2025 23:02:45 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f23beae460e2708631a53cb8cd2af35961c5d5f349c84c721e2a8086900de98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264787439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c0bb3b86a0374fd06c8ee1c1fb4719f8a2a1c4c8c2361141aa8bce9cd0669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c0f47338b353fb5108e63ba21f537e410d3adc552ada9dc6c79cc939a752d`  
		Last Modified: Wed, 08 Oct 2025 20:18:25 GMT  
		Size: 5.9 MB (5878120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077e9399fc8d6edf70bca86e878d6c21d631ab38ea31043f266040cb086afdf5`  
		Last Modified: Wed, 08 Oct 2025 20:17:57 GMT  
		Size: 229.7 MB (229699316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52568e110dd581bd9967bf126633450eac3ccab20598c6ae9a1d6f68fe9e326`  
		Last Modified: Wed, 08 Oct 2025 20:18:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1872746b5da92b8f9dfd97fef1370b4e1005521741d180cacd0c89f3bf8cb0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699abf8319ba3b4cf8234888f9a258fa360d4dc15eb0986f2097d1a39bf2758e`

```dockerfile
```

-	Layers:
	-	`sha256:3a00f81b981ec175e6d7695807b6b5bb2bc871645ec3694439d9cfa733479c2b`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f04ed6bb80e87a156b6f93281ea06fb604b3fe93b5ec49d27a31d503d5acff`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-trixie`

```console
$ docker pull julia@sha256:5b0938cb249a46258dc3c0dfa4541829ef2811dfbcf0b0c4272feccce7074dd0
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
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:743d12f48c5e16cb9bfc0a8ea9fa3a500d8dc65a90e424a38994874724126c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:86957bc28b8cbc3c9df766b39ba1f643f57055b89c1e34c9f87f1c110ba899ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:a4720044b1d9b33354bdba6060ce8864927053db2fa365144a263cb7eb3a4c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:7041e8ae1847cb0eaea4d96390b2eac25bd2471cf40c2a3b274afc9a0c455a52
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
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:9bdd2e8d822585ae438fef96106f4f82cccb703cd7ca945a4c99f628e4793b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef3f3b8f858a875c7d5f98f69f7917a5fc6c69b46387946144032d99e9f487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707d58098b48b1282a096b0cc43a742bb413762e984b0d4977680d4ae12da6`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 6.2 MB (6242822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0144b6cd8f232595608450312327d15baeaba8112806778d8500a106a30b877e`  
		Last Modified: Tue, 30 Sep 2025 03:00:15 GMT  
		Size: 176.4 MB (176362247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d54c2099e5a781a654e3d4e9fc78b69f251699777e1aa9fd27b3114c7bdcd1`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:5b92289408cd2e9634f67a8bb95ac0d8fec7feec820f5f4b46f34cdab481b989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3722500dab1d1bb74004e572577c52c339597f86ada79b8c9a40f77568fbb6`

```dockerfile
```

-	Layers:
	-	`sha256:b6582600941bd55bc9515a5b5d9c81c5ece79c072569fdbd5cdf02da4b0ee99c`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 2.2 MB (2240099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ffb549b8e93ab6069ddf4310cab2995edb4a47ef7b19ffed7985885f781df81`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ea2e89e2c68a1aa87cef5d58f6c6c4a9fd72dadde64dc65bf1f4c5d02cd7551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213744371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffef92cd6b6877ee5bb5648ba20a6bea4d4316d60861afd4969b716c87b70a10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24134d35066eccc57f1cfd9ea3628f2f0bd08dd14b257200d3f308d3cfa9649f`  
		Last Modified: Mon, 29 Sep 2025 23:56:29 GMT  
		Size: 6.2 MB (6153035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b4bd31b16e44c7f444d0424964e663523aa2a6a9a67cb3e2580a1da979271`  
		Last Modified: Tue, 30 Sep 2025 11:48:58 GMT  
		Size: 177.5 MB (177450122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85ef13ddde40c480fddcf7fe6f2fb64ea19c5ff25aa57216acd983a31ab2eb`  
		Last Modified: Mon, 29 Sep 2025 23:56:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:768330402ab6a5b7101096a6781bf79e0c79a220824fa0ddf8f26605e3513f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1807bf8b6bc8e2a448c1448f6b7fc33e99175be9147e7a95272d2ab74149e8b8`

```dockerfile
```

-	Layers:
	-	`sha256:a146189b1be62d10ecf4e2d4d0b421ff0b4532edb681c86d7c8bd97dca30ac75`  
		Last Modified: Tue, 30 Sep 2025 02:02:57 GMT  
		Size: 2.2 MB (2239149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb85f3f31926fa13b79f284fd226b9047ad4eb33cdf23a7c51725250d97e6f6`  
		Last Modified: Tue, 30 Sep 2025 02:02:58 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:ec57c259586605864e41423b8bda7fba131a10b0c655694d4f0e6ee19e71fc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb080987b44fe22f2d5fc329198b2f071fbdc168ab2a785b3412845dd12fb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7653834ba0a8a0acd1b09ab2c5f73ea430d1c5ea9b14a623ae0dc9a67e567128`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c835f063247ee20f910ca6b88d312a9262311f206a046418e14d7904433f1`  
		Last Modified: Tue, 30 Sep 2025 20:22:52 GMT  
		Size: 157.8 MB (157841832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97896db05c9a7c73c76f3699521152eccd99ec03d6afb9763eb702d22726b282`  
		Last Modified: Mon, 29 Sep 2025 23:56:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:5f86066e6ba7e263f7806760b4d95ff1bff5385fa55180e3ab55543cd3e79c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6318a864e3966d428b4e40272c2f9213b7befa20d17d8b1165d3ab321a6ae`

```dockerfile
```

-	Layers:
	-	`sha256:d42c2e787f2a387ce69818eb8d50469e94874c6b37f543dd9e0f04650a54e63a`  
		Last Modified: Tue, 30 Sep 2025 02:03:02 GMT  
		Size: 2.2 MB (2237244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa85468960b4c41127cd8ac60229fa3d681c7c036806068ad7ae688d74daab`  
		Last Modified: Tue, 30 Sep 2025 02:03:03 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:30d84856fd171760ce0a9862d1a33e552daaa338eb37c8f9baaa54f982bf39a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eddcb1f0f78a269edb3bbe11ca9baf096a3516c9746b72f91b3ca95475b8086`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e049a22458b36b2d3ea4032641756768b7a2948255b7d1190bc00cee73fa5`  
		Last Modified: Wed, 01 Oct 2025 19:50:16 GMT  
		Size: 155.4 MB (155388263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e7bc991b97ad3c3b076d2e166c04773f1f7eef81c48fd801f6c80e8e778a1`  
		Last Modified: Tue, 30 Sep 2025 06:59:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:92a5e8ad68115edc663db39f6f57857a37bf29c0d90a170c11329e0ff53129a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b9005e68dbb4df1cccbad1ae0683c6efe0fd05282f13c292f6bbd7af9982b`

```dockerfile
```

-	Layers:
	-	`sha256:a8ae5b88e9b657ffd7db9a58e5fb73d94bd18ae5636fcf9bec841a59e7401680`  
		Last Modified: Wed, 01 Oct 2025 20:02:37 GMT  
		Size: 2.2 MB (2242594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a22e7cf4697522c5969d96f8a3688f4cf6dd3860122004d29e476e8bcdfd3f`  
		Last Modified: Wed, 01 Oct 2025 20:02:38 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:da67cbb6230b4b9dcabb30a422c650d00461f556f32a1f3be39997471f37def3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3760210945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b1c0f868905a5338a67c399a13a5d62242912efac8938c789540dbac48b3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:36 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d87d05a897bccb5f2b7b0f22a2b7312f68dc3c05d98e93bd4b174511375fd`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9eaf5fcd45138239d877efa9dac052ec12bcacbc692aae3bef9bdacfe29c4`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa8b00aad4e24b567fd98cb2aae6e70687f65c9e58d30bbbc43ffbbd51066e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85846a480db99cf371627c3469d0766b75967b3d53e637cfaecd0d139873917d`  
		Last Modified: Wed, 10 Sep 2025 23:03:15 GMT  
		Size: 188.8 MB (188764648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dadd3c915b1707b2d227974d8bb0390fddf3d5d51303c0818a22048e0b6d7`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:be47fca4d707b05e29ce3ff64816d89d3804c3c57637f597808fa1da7bb2267b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470929970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2ef2f42509e55312e4a99a4f497a610248e3a544b25ac6181575751bd98b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:09 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:11 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e1324c130b59cc18854ac448cfe66bbdc6ea607d02d5a5efddbcbb3ccf199`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f6fdb153be7a554e4d0138b415168278f965f1a7ffe38c39dfd74aae2c5d2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc520230594198d2f30051a2544a775e109761bb519daa250651f7725fc796`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409404ed358ab10b3cdc090e5c12846484bec36fdd3bc479b22ae1b4c40797`  
		Last Modified: Wed, 10 Sep 2025 23:03:11 GMT  
		Size: 188.8 MB (188778455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06419495af2c922b2789cc1b07e6ddf74173cf1485fd4aa8f838f47f3552f1c2`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:a8f5af46772bd26fdd04ac37ce2b7571ab94ef5273ba8e36873c865a9a50f8d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:f421b9479b521f3d62a1b28e59c7dfe0fc6bec65908fcbe259f560f810200be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182099328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f096177342cde9495e2b22588334a40d47ed97f82763c5488f6e16f22019b84c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539647b7ad1c52bae4fa8c75d78308de54a19346b07a2ab5cd43cf0560807b17`  
		Last Modified: Wed, 16 Jul 2025 01:43:33 GMT  
		Size: 178.3 MB (178299271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8ac956161de79b643ed29fc037ea0265da3a1e230177bc891bc4a8426a259`  
		Last Modified: Tue, 15 Jul 2025 19:13:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:8a482dd06daaa09afcf49f62e40163089dc1d2f1007b670a163f567f27b8fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef5862c20f5a505305ea8778406a2e4472f29db92433706af3515d1af23728`

```dockerfile
```

-	Layers:
	-	`sha256:e935d791e7ea2f3554bae8322d7ea0c97a0a73aaee701eee9a9c6a2e90b782c0`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94bc44c63e95d54ce3cb84e01ae72359db47a277d48a052d040c733fae44475`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:5ba34c84f812e38f5c00c5dea2f103fc5871421ac032da823ecbb2817a91b2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:8642d4cca1d693d6173c2d3e8e735764a8ac334f9e0fffab6b89751a1271391d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181936816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a90a19868152d78d2b911934b6fcba87551d73e5bf9a9be6d4d33e5750a6dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa55b07cde92d1829b335fc35e6c108502913fc8d43afdc266f62dfba47be8b`  
		Last Modified: Wed, 16 Jul 2025 01:44:05 GMT  
		Size: 178.3 MB (178298876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700fd2f654a8766de3e5c00b62c9e1197c24baccefcf8a23752bc6624c241b06`  
		Last Modified: Tue, 15 Jul 2025 19:13:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:5a38baca73ea576e7103dae3236945648e9f0eacaa4054b10426e7c286f1c704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae6717b55611342b0c609d9e361a195274b507e99018851c7b33f6911b8a3e4`

```dockerfile
```

-	Layers:
	-	`sha256:1fb548b669aab7837e29582969c87159ddc91961f6f01c78b8993511dfe420e3`  
		Last Modified: Tue, 15 Jul 2025 23:02:31 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14e44b46941444714887e63fe9cd70859585689bed49a75ea0653bf90f5be2d`  
		Last Modified: Tue, 15 Jul 2025 23:02:32 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.22`

```console
$ docker pull julia@sha256:a8f5af46772bd26fdd04ac37ce2b7571ab94ef5273ba8e36873c865a9a50f8d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:f421b9479b521f3d62a1b28e59c7dfe0fc6bec65908fcbe259f560f810200be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182099328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f096177342cde9495e2b22588334a40d47ed97f82763c5488f6e16f22019b84c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539647b7ad1c52bae4fa8c75d78308de54a19346b07a2ab5cd43cf0560807b17`  
		Last Modified: Wed, 16 Jul 2025 01:43:33 GMT  
		Size: 178.3 MB (178299271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8ac956161de79b643ed29fc037ea0265da3a1e230177bc891bc4a8426a259`  
		Last Modified: Tue, 15 Jul 2025 19:13:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:8a482dd06daaa09afcf49f62e40163089dc1d2f1007b670a163f567f27b8fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef5862c20f5a505305ea8778406a2e4472f29db92433706af3515d1af23728`

```dockerfile
```

-	Layers:
	-	`sha256:e935d791e7ea2f3554bae8322d7ea0c97a0a73aaee701eee9a9c6a2e90b782c0`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94bc44c63e95d54ce3cb84e01ae72359db47a277d48a052d040c733fae44475`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:d2fbea2d62543a7e54733de0360740e1da7859202c9f19de602997ade615d272
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
$ docker pull julia@sha256:1f520d165111ad0b1d03bdd673f12dbfdedd8bdd2ca9177d7edd922cafd3fd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405db8ae01d7a24ed7df98e9d1fe2595b01d2319eb5afb12d59db71953bb96bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d207494e65395b462e83b1c8cb991f719c2d2f632afe07bb609289b6977ed`  
		Last Modified: Mon, 29 Sep 2025 23:56:18 GMT  
		Size: 5.7 MB (5716224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b39a0c985fb6ec837cdfb0de0411920898db318dfd9a2e9a022a434b4f22ce9`  
		Last Modified: Tue, 30 Sep 2025 03:34:36 GMT  
		Size: 176.3 MB (176324333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6379b701977ee040c82d96a4dee769b4816d4b37f192bd07265c6bd1284ddda`  
		Last Modified: Mon, 29 Sep 2025 23:56:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bc7df85a3f599d274c464601443773f0ab8637afe9c9d3391770948b71c9f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d50c7f89a06ea9395429b886245273b89b7aed74f337b6d8b1f4e970a5f3b9`

```dockerfile
```

-	Layers:
	-	`sha256:d2cf12cedf5c3c8639f768ca3f75dbc4897f062b2e5200449cb9792f811cc7fc`  
		Last Modified: Tue, 30 Sep 2025 02:03:06 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268dcad5982db2c20530b19e5be820cb5fa032883dae77005422f9930a6b1a5e`  
		Last Modified: Tue, 30 Sep 2025 02:03:07 GMT  
		Size: 16.6 KB (16641 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c49dc5f45776c0d100db5b086f6c54c23bd620d0e7543a159452354545a1e2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747d0bcf54a8c42e56b8cdd4d84f10cf70348637de5234c18b8ad0400ca88ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22faea7eae410e22e76d8d8ecf1e7479df19c2feca6920129c88123a2983c77b`  
		Last Modified: Tue, 30 Sep 2025 14:52:31 GMT  
		Size: 5.6 MB (5567126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75663d3a523baf385914288571496f152eda4d27fa6b8793f0d98df87a9e242`  
		Last Modified: Tue, 30 Sep 2025 14:52:37 GMT  
		Size: 177.4 MB (177412369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3e482aa54d18d1ecb2b8bb984385089d3d7905dbef00ed8be0626a86f54c8a`  
		Last Modified: Tue, 30 Sep 2025 00:40:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9297f47b0901ac1f0416670abc684a7f1da3d6d7261ef7e2344f1f5cf453ed78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9534bc50ebb2526afd67f835364914bf33db8f53791d2e9a2fc386102835ab73`

```dockerfile
```

-	Layers:
	-	`sha256:751bc869bb0837e2c3b7b4b37923b114bcc822c59715ac6bf16f7b47fac5328a`  
		Last Modified: Tue, 30 Sep 2025 02:03:11 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de3b3d4762f479d244698d0611be0f762d6b62df02a2790063590d769ba70a7`  
		Last Modified: Tue, 30 Sep 2025 02:03:12 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d5178629204b5c199bdaf495ce91fc63c9ca35053bac4b400afe2b2e6dd02c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192895936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30d250ef264455e19c57e8a865a0a7e6670759cbd2c1e059650ae2d7276c75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c05b711baf2fbb0ea28f1471b9c21eccfbd1afbc38f720524210adafa7cbf`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 5.9 MB (5878055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b1bd6618c529345329aaef39117bbebb05c2a1b97d5b5e8af355b7ee2b77a`  
		Last Modified: Tue, 30 Sep 2025 20:22:46 GMT  
		Size: 157.8 MB (157807881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9927a86c8e920937918dad744f3a35b882c69d3af1dbe1e816a67fdabe983f`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9be026b01a496eb718b203f93742bce6d63cc1605e6fa920c4f7999ca54a9d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44456cac65eb6e4a40b596f12e071f09c3b31169d4a875f75f8c35731b45a003`

```dockerfile
```

-	Layers:
	-	`sha256:f35ae8c2a93ff712162de5397645e375fba332fadccad32202f18b06fbe709aa`  
		Last Modified: Tue, 30 Sep 2025 02:03:16 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238be5b9615499321f8af30e5715b8d2f49995f7b766c9a94e7081a432db0b57`  
		Last Modified: Tue, 30 Sep 2025 02:03:16 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3c831cbfedc06f4fd17f396abb9bb1e323f9bae45253583be3e9210c645ea357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9830c8a7199b60f02e771383bb11cbd5c2fbbebaa9ee9f6907303dd29545352`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae5078f4b42d42980e7af775968ea12030fa58a473b5ada40edb06ba780153`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 6.3 MB (6256416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12db94eacc45cb74a1164c1edb5292200eaa5321ee2fa5e8b8d7ec2e31fa4ca9`  
		Last Modified: Tue, 30 Sep 2025 20:22:46 GMT  
		Size: 155.4 MB (155354786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d695276160cee404b93676a5ab642c5707cb4bef86f31283eca2a79f3795`  
		Last Modified: Mon, 29 Sep 2025 23:57:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5215cac9e887a1f245da35205d53118278161c0b4ff2dcc7f9497f9483b8633b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca60ac1a58d7cb1a4e3b17394190dbef116ab3cc67d63a50a6a9164de848c7c`

```dockerfile
```

-	Layers:
	-	`sha256:27637cae709f0f79bb0bf3c4f7ddd66d2d170533fdb50c094fea2d24594cc843`  
		Last Modified: Tue, 30 Sep 2025 02:03:20 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9dce671a122e86edda90327444044a49844a1803e15371bda704b0aa762589`  
		Last Modified: Tue, 30 Sep 2025 02:03:21 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-trixie`

```console
$ docker pull julia@sha256:49526ad6e28ba6129e3063100904c355b237ff47b73dadb476e0513f0a98575d
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
$ docker pull julia@sha256:9bdd2e8d822585ae438fef96106f4f82cccb703cd7ca945a4c99f628e4793b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef3f3b8f858a875c7d5f98f69f7917a5fc6c69b46387946144032d99e9f487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707d58098b48b1282a096b0cc43a742bb413762e984b0d4977680d4ae12da6`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 6.2 MB (6242822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0144b6cd8f232595608450312327d15baeaba8112806778d8500a106a30b877e`  
		Last Modified: Tue, 30 Sep 2025 03:00:15 GMT  
		Size: 176.4 MB (176362247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d54c2099e5a781a654e3d4e9fc78b69f251699777e1aa9fd27b3114c7bdcd1`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5b92289408cd2e9634f67a8bb95ac0d8fec7feec820f5f4b46f34cdab481b989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3722500dab1d1bb74004e572577c52c339597f86ada79b8c9a40f77568fbb6`

```dockerfile
```

-	Layers:
	-	`sha256:b6582600941bd55bc9515a5b5d9c81c5ece79c072569fdbd5cdf02da4b0ee99c`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 2.2 MB (2240099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ffb549b8e93ab6069ddf4310cab2995edb4a47ef7b19ffed7985885f781df81`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ea2e89e2c68a1aa87cef5d58f6c6c4a9fd72dadde64dc65bf1f4c5d02cd7551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213744371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffef92cd6b6877ee5bb5648ba20a6bea4d4316d60861afd4969b716c87b70a10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24134d35066eccc57f1cfd9ea3628f2f0bd08dd14b257200d3f308d3cfa9649f`  
		Last Modified: Mon, 29 Sep 2025 23:56:29 GMT  
		Size: 6.2 MB (6153035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b4bd31b16e44c7f444d0424964e663523aa2a6a9a67cb3e2580a1da979271`  
		Last Modified: Tue, 30 Sep 2025 11:48:58 GMT  
		Size: 177.5 MB (177450122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85ef13ddde40c480fddcf7fe6f2fb64ea19c5ff25aa57216acd983a31ab2eb`  
		Last Modified: Mon, 29 Sep 2025 23:56:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:768330402ab6a5b7101096a6781bf79e0c79a220824fa0ddf8f26605e3513f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1807bf8b6bc8e2a448c1448f6b7fc33e99175be9147e7a95272d2ab74149e8b8`

```dockerfile
```

-	Layers:
	-	`sha256:a146189b1be62d10ecf4e2d4d0b421ff0b4532edb681c86d7c8bd97dca30ac75`  
		Last Modified: Tue, 30 Sep 2025 02:02:57 GMT  
		Size: 2.2 MB (2239149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb85f3f31926fa13b79f284fd226b9047ad4eb33cdf23a7c51725250d97e6f6`  
		Last Modified: Tue, 30 Sep 2025 02:02:58 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:ec57c259586605864e41423b8bda7fba131a10b0c655694d4f0e6ee19e71fc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb080987b44fe22f2d5fc329198b2f071fbdc168ab2a785b3412845dd12fb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7653834ba0a8a0acd1b09ab2c5f73ea430d1c5ea9b14a623ae0dc9a67e567128`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c835f063247ee20f910ca6b88d312a9262311f206a046418e14d7904433f1`  
		Last Modified: Tue, 30 Sep 2025 20:22:52 GMT  
		Size: 157.8 MB (157841832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97896db05c9a7c73c76f3699521152eccd99ec03d6afb9763eb702d22726b282`  
		Last Modified: Mon, 29 Sep 2025 23:56:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5f86066e6ba7e263f7806760b4d95ff1bff5385fa55180e3ab55543cd3e79c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6318a864e3966d428b4e40272c2f9213b7befa20d17d8b1165d3ab321a6ae`

```dockerfile
```

-	Layers:
	-	`sha256:d42c2e787f2a387ce69818eb8d50469e94874c6b37f543dd9e0f04650a54e63a`  
		Last Modified: Tue, 30 Sep 2025 02:03:02 GMT  
		Size: 2.2 MB (2237244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa85468960b4c41127cd8ac60229fa3d681c7c036806068ad7ae688d74daab`  
		Last Modified: Tue, 30 Sep 2025 02:03:03 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:30d84856fd171760ce0a9862d1a33e552daaa338eb37c8f9baaa54f982bf39a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eddcb1f0f78a269edb3bbe11ca9baf096a3516c9746b72f91b3ca95475b8086`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e049a22458b36b2d3ea4032641756768b7a2948255b7d1190bc00cee73fa5`  
		Last Modified: Wed, 01 Oct 2025 19:50:16 GMT  
		Size: 155.4 MB (155388263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e7bc991b97ad3c3b076d2e166c04773f1f7eef81c48fd801f6c80e8e778a1`  
		Last Modified: Tue, 30 Sep 2025 06:59:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:92a5e8ad68115edc663db39f6f57857a37bf29c0d90a170c11329e0ff53129a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b9005e68dbb4df1cccbad1ae0683c6efe0fd05282f13c292f6bbd7af9982b`

```dockerfile
```

-	Layers:
	-	`sha256:a8ae5b88e9b657ffd7db9a58e5fb73d94bd18ae5636fcf9bec841a59e7401680`  
		Last Modified: Wed, 01 Oct 2025 20:02:37 GMT  
		Size: 2.2 MB (2242594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a22e7cf4697522c5969d96f8a3688f4cf6dd3860122004d29e476e8bcdfd3f`  
		Last Modified: Wed, 01 Oct 2025 20:02:38 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:28acbfc3b79a13146552c59a17f82fc89afcf2598f0c21327f361cf44068ec4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:da67cbb6230b4b9dcabb30a422c650d00461f556f32a1f3be39997471f37def3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3760210945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b1c0f868905a5338a67c399a13a5d62242912efac8938c789540dbac48b3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:36 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d87d05a897bccb5f2b7b0f22a2b7312f68dc3c05d98e93bd4b174511375fd`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9eaf5fcd45138239d877efa9dac052ec12bcacbc692aae3bef9bdacfe29c4`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa8b00aad4e24b567fd98cb2aae6e70687f65c9e58d30bbbc43ffbbd51066e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85846a480db99cf371627c3469d0766b75967b3d53e637cfaecd0d139873917d`  
		Last Modified: Wed, 10 Sep 2025 23:03:15 GMT  
		Size: 188.8 MB (188764648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dadd3c915b1707b2d227974d8bb0390fddf3d5d51303c0818a22048e0b6d7`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:be47fca4d707b05e29ce3ff64816d89d3804c3c57637f597808fa1da7bb2267b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470929970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2ef2f42509e55312e4a99a4f497a610248e3a544b25ac6181575751bd98b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:09 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:11 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e1324c130b59cc18854ac448cfe66bbdc6ea607d02d5a5efddbcbb3ccf199`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f6fdb153be7a554e4d0138b415168278f965f1a7ffe38c39dfd74aae2c5d2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc520230594198d2f30051a2544a775e109761bb519daa250651f7725fc796`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409404ed358ab10b3cdc090e5c12846484bec36fdd3bc479b22ae1b4c40797`  
		Last Modified: Wed, 10 Sep 2025 23:03:11 GMT  
		Size: 188.8 MB (188778455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06419495af2c922b2789cc1b07e6ddf74173cf1485fd4aa8f838f47f3552f1c2`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5fd0a141c8fe1b45fdb1e320c793b7442c52ca7fd73d3d4acaedf587d6dc2fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:be47fca4d707b05e29ce3ff64816d89d3804c3c57637f597808fa1da7bb2267b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470929970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2ef2f42509e55312e4a99a4f497a610248e3a544b25ac6181575751bd98b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:09 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:11 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e1324c130b59cc18854ac448cfe66bbdc6ea607d02d5a5efddbcbb3ccf199`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f6fdb153be7a554e4d0138b415168278f965f1a7ffe38c39dfd74aae2c5d2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc520230594198d2f30051a2544a775e109761bb519daa250651f7725fc796`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409404ed358ab10b3cdc090e5c12846484bec36fdd3bc479b22ae1b4c40797`  
		Last Modified: Wed, 10 Sep 2025 23:03:11 GMT  
		Size: 188.8 MB (188778455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06419495af2c922b2789cc1b07e6ddf74173cf1485fd4aa8f838f47f3552f1c2`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:6c18cb8bfa4a2f34a25e804b641c19183540d1b115f623bce3d3b8a6d96a7673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:da67cbb6230b4b9dcabb30a422c650d00461f556f32a1f3be39997471f37def3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3760210945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b1c0f868905a5338a67c399a13a5d62242912efac8938c789540dbac48b3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:36 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d87d05a897bccb5f2b7b0f22a2b7312f68dc3c05d98e93bd4b174511375fd`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9eaf5fcd45138239d877efa9dac052ec12bcacbc692aae3bef9bdacfe29c4`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa8b00aad4e24b567fd98cb2aae6e70687f65c9e58d30bbbc43ffbbd51066e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85846a480db99cf371627c3469d0766b75967b3d53e637cfaecd0d139873917d`  
		Last Modified: Wed, 10 Sep 2025 23:03:15 GMT  
		Size: 188.8 MB (188764648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dadd3c915b1707b2d227974d8bb0390fddf3d5d51303c0818a22048e0b6d7`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10`

```console
$ docker pull julia@sha256:7041e8ae1847cb0eaea4d96390b2eac25bd2471cf40c2a3b274afc9a0c455a52
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
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.10.10` - linux; amd64

```console
$ docker pull julia@sha256:9bdd2e8d822585ae438fef96106f4f82cccb703cd7ca945a4c99f628e4793b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef3f3b8f858a875c7d5f98f69f7917a5fc6c69b46387946144032d99e9f487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707d58098b48b1282a096b0cc43a742bb413762e984b0d4977680d4ae12da6`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 6.2 MB (6242822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0144b6cd8f232595608450312327d15baeaba8112806778d8500a106a30b877e`  
		Last Modified: Tue, 30 Sep 2025 03:00:15 GMT  
		Size: 176.4 MB (176362247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d54c2099e5a781a654e3d4e9fc78b69f251699777e1aa9fd27b3114c7bdcd1`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:5b92289408cd2e9634f67a8bb95ac0d8fec7feec820f5f4b46f34cdab481b989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3722500dab1d1bb74004e572577c52c339597f86ada79b8c9a40f77568fbb6`

```dockerfile
```

-	Layers:
	-	`sha256:b6582600941bd55bc9515a5b5d9c81c5ece79c072569fdbd5cdf02da4b0ee99c`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 2.2 MB (2240099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ffb549b8e93ab6069ddf4310cab2995edb4a47ef7b19ffed7985885f781df81`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ea2e89e2c68a1aa87cef5d58f6c6c4a9fd72dadde64dc65bf1f4c5d02cd7551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213744371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffef92cd6b6877ee5bb5648ba20a6bea4d4316d60861afd4969b716c87b70a10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24134d35066eccc57f1cfd9ea3628f2f0bd08dd14b257200d3f308d3cfa9649f`  
		Last Modified: Mon, 29 Sep 2025 23:56:29 GMT  
		Size: 6.2 MB (6153035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b4bd31b16e44c7f444d0424964e663523aa2a6a9a67cb3e2580a1da979271`  
		Last Modified: Tue, 30 Sep 2025 11:48:58 GMT  
		Size: 177.5 MB (177450122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85ef13ddde40c480fddcf7fe6f2fb64ea19c5ff25aa57216acd983a31ab2eb`  
		Last Modified: Mon, 29 Sep 2025 23:56:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:768330402ab6a5b7101096a6781bf79e0c79a220824fa0ddf8f26605e3513f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1807bf8b6bc8e2a448c1448f6b7fc33e99175be9147e7a95272d2ab74149e8b8`

```dockerfile
```

-	Layers:
	-	`sha256:a146189b1be62d10ecf4e2d4d0b421ff0b4532edb681c86d7c8bd97dca30ac75`  
		Last Modified: Tue, 30 Sep 2025 02:02:57 GMT  
		Size: 2.2 MB (2239149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb85f3f31926fa13b79f284fd226b9047ad4eb33cdf23a7c51725250d97e6f6`  
		Last Modified: Tue, 30 Sep 2025 02:02:58 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; 386

```console
$ docker pull julia@sha256:ec57c259586605864e41423b8bda7fba131a10b0c655694d4f0e6ee19e71fc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb080987b44fe22f2d5fc329198b2f071fbdc168ab2a785b3412845dd12fb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7653834ba0a8a0acd1b09ab2c5f73ea430d1c5ea9b14a623ae0dc9a67e567128`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c835f063247ee20f910ca6b88d312a9262311f206a046418e14d7904433f1`  
		Last Modified: Tue, 30 Sep 2025 20:22:52 GMT  
		Size: 157.8 MB (157841832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97896db05c9a7c73c76f3699521152eccd99ec03d6afb9763eb702d22726b282`  
		Last Modified: Mon, 29 Sep 2025 23:56:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:5f86066e6ba7e263f7806760b4d95ff1bff5385fa55180e3ab55543cd3e79c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6318a864e3966d428b4e40272c2f9213b7befa20d17d8b1165d3ab321a6ae`

```dockerfile
```

-	Layers:
	-	`sha256:d42c2e787f2a387ce69818eb8d50469e94874c6b37f543dd9e0f04650a54e63a`  
		Last Modified: Tue, 30 Sep 2025 02:03:02 GMT  
		Size: 2.2 MB (2237244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa85468960b4c41127cd8ac60229fa3d681c7c036806068ad7ae688d74daab`  
		Last Modified: Tue, 30 Sep 2025 02:03:03 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; ppc64le

```console
$ docker pull julia@sha256:30d84856fd171760ce0a9862d1a33e552daaa338eb37c8f9baaa54f982bf39a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eddcb1f0f78a269edb3bbe11ca9baf096a3516c9746b72f91b3ca95475b8086`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e049a22458b36b2d3ea4032641756768b7a2948255b7d1190bc00cee73fa5`  
		Last Modified: Wed, 01 Oct 2025 19:50:16 GMT  
		Size: 155.4 MB (155388263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e7bc991b97ad3c3b076d2e166c04773f1f7eef81c48fd801f6c80e8e778a1`  
		Last Modified: Tue, 30 Sep 2025 06:59:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:92a5e8ad68115edc663db39f6f57857a37bf29c0d90a170c11329e0ff53129a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b9005e68dbb4df1cccbad1ae0683c6efe0fd05282f13c292f6bbd7af9982b`

```dockerfile
```

-	Layers:
	-	`sha256:a8ae5b88e9b657ffd7db9a58e5fb73d94bd18ae5636fcf9bec841a59e7401680`  
		Last Modified: Wed, 01 Oct 2025 20:02:37 GMT  
		Size: 2.2 MB (2242594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a22e7cf4697522c5969d96f8a3688f4cf6dd3860122004d29e476e8bcdfd3f`  
		Last Modified: Wed, 01 Oct 2025 20:02:38 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:da67cbb6230b4b9dcabb30a422c650d00461f556f32a1f3be39997471f37def3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3760210945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b1c0f868905a5338a67c399a13a5d62242912efac8938c789540dbac48b3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:36 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d87d05a897bccb5f2b7b0f22a2b7312f68dc3c05d98e93bd4b174511375fd`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9eaf5fcd45138239d877efa9dac052ec12bcacbc692aae3bef9bdacfe29c4`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa8b00aad4e24b567fd98cb2aae6e70687f65c9e58d30bbbc43ffbbd51066e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85846a480db99cf371627c3469d0766b75967b3d53e637cfaecd0d139873917d`  
		Last Modified: Wed, 10 Sep 2025 23:03:15 GMT  
		Size: 188.8 MB (188764648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dadd3c915b1707b2d227974d8bb0390fddf3d5d51303c0818a22048e0b6d7`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:be47fca4d707b05e29ce3ff64816d89d3804c3c57637f597808fa1da7bb2267b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470929970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2ef2f42509e55312e4a99a4f497a610248e3a544b25ac6181575751bd98b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:09 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:11 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e1324c130b59cc18854ac448cfe66bbdc6ea607d02d5a5efddbcbb3ccf199`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f6fdb153be7a554e4d0138b415168278f965f1a7ffe38c39dfd74aae2c5d2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc520230594198d2f30051a2544a775e109761bb519daa250651f7725fc796`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409404ed358ab10b3cdc090e5c12846484bec36fdd3bc479b22ae1b4c40797`  
		Last Modified: Wed, 10 Sep 2025 23:03:11 GMT  
		Size: 188.8 MB (188778455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06419495af2c922b2789cc1b07e6ddf74173cf1485fd4aa8f838f47f3552f1c2`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-alpine`

```console
$ docker pull julia@sha256:a8f5af46772bd26fdd04ac37ce2b7571ab94ef5273ba8e36873c865a9a50f8d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:f421b9479b521f3d62a1b28e59c7dfe0fc6bec65908fcbe259f560f810200be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182099328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f096177342cde9495e2b22588334a40d47ed97f82763c5488f6e16f22019b84c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539647b7ad1c52bae4fa8c75d78308de54a19346b07a2ab5cd43cf0560807b17`  
		Last Modified: Wed, 16 Jul 2025 01:43:33 GMT  
		Size: 178.3 MB (178299271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8ac956161de79b643ed29fc037ea0265da3a1e230177bc891bc4a8426a259`  
		Last Modified: Tue, 15 Jul 2025 19:13:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:8a482dd06daaa09afcf49f62e40163089dc1d2f1007b670a163f567f27b8fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef5862c20f5a505305ea8778406a2e4472f29db92433706af3515d1af23728`

```dockerfile
```

-	Layers:
	-	`sha256:e935d791e7ea2f3554bae8322d7ea0c97a0a73aaee701eee9a9c6a2e90b782c0`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94bc44c63e95d54ce3cb84e01ae72359db47a277d48a052d040c733fae44475`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.21`

```console
$ docker pull julia@sha256:5ba34c84f812e38f5c00c5dea2f103fc5871421ac032da823ecbb2817a91b2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:8642d4cca1d693d6173c2d3e8e735764a8ac334f9e0fffab6b89751a1271391d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181936816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a90a19868152d78d2b911934b6fcba87551d73e5bf9a9be6d4d33e5750a6dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa55b07cde92d1829b335fc35e6c108502913fc8d43afdc266f62dfba47be8b`  
		Last Modified: Wed, 16 Jul 2025 01:44:05 GMT  
		Size: 178.3 MB (178298876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700fd2f654a8766de3e5c00b62c9e1197c24baccefcf8a23752bc6624c241b06`  
		Last Modified: Tue, 15 Jul 2025 19:13:52 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:5a38baca73ea576e7103dae3236945648e9f0eacaa4054b10426e7c286f1c704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae6717b55611342b0c609d9e361a195274b507e99018851c7b33f6911b8a3e4`

```dockerfile
```

-	Layers:
	-	`sha256:1fb548b669aab7837e29582969c87159ddc91961f6f01c78b8993511dfe420e3`  
		Last Modified: Tue, 15 Jul 2025 23:02:31 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14e44b46941444714887e63fe9cd70859585689bed49a75ea0653bf90f5be2d`  
		Last Modified: Tue, 15 Jul 2025 23:02:32 GMT  
		Size: 12.0 KB (11971 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.22`

```console
$ docker pull julia@sha256:a8f5af46772bd26fdd04ac37ce2b7571ab94ef5273ba8e36873c865a9a50f8d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:f421b9479b521f3d62a1b28e59c7dfe0fc6bec65908fcbe259f560f810200be2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182099328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f096177342cde9495e2b22588334a40d47ed97f82763c5488f6e16f22019b84c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
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
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539647b7ad1c52bae4fa8c75d78308de54a19346b07a2ab5cd43cf0560807b17`  
		Last Modified: Wed, 16 Jul 2025 01:43:33 GMT  
		Size: 178.3 MB (178299271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb8ac956161de79b643ed29fc037ea0265da3a1e230177bc891bc4a8426a259`  
		Last Modified: Tue, 15 Jul 2025 19:13:40 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:8a482dd06daaa09afcf49f62e40163089dc1d2f1007b670a163f567f27b8fd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef5862c20f5a505305ea8778406a2e4472f29db92433706af3515d1af23728`

```dockerfile
```

-	Layers:
	-	`sha256:e935d791e7ea2f3554bae8322d7ea0c97a0a73aaee701eee9a9c6a2e90b782c0`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94bc44c63e95d54ce3cb84e01ae72359db47a277d48a052d040c733fae44475`  
		Last Modified: Tue, 15 Jul 2025 23:02:29 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-bookworm`

```console
$ docker pull julia@sha256:d2fbea2d62543a7e54733de0360740e1da7859202c9f19de602997ade615d272
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
$ docker pull julia@sha256:1f520d165111ad0b1d03bdd673f12dbfdedd8bdd2ca9177d7edd922cafd3fd71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405db8ae01d7a24ed7df98e9d1fe2595b01d2319eb5afb12d59db71953bb96bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d207494e65395b462e83b1c8cb991f719c2d2f632afe07bb609289b6977ed`  
		Last Modified: Mon, 29 Sep 2025 23:56:18 GMT  
		Size: 5.7 MB (5716224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b39a0c985fb6ec837cdfb0de0411920898db318dfd9a2e9a022a434b4f22ce9`  
		Last Modified: Tue, 30 Sep 2025 03:34:36 GMT  
		Size: 176.3 MB (176324333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6379b701977ee040c82d96a4dee769b4816d4b37f192bd07265c6bd1284ddda`  
		Last Modified: Mon, 29 Sep 2025 23:56:17 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bc7df85a3f599d274c464601443773f0ab8637afe9c9d3391770948b71c9f73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d50c7f89a06ea9395429b886245273b89b7aed74f337b6d8b1f4e970a5f3b9`

```dockerfile
```

-	Layers:
	-	`sha256:d2cf12cedf5c3c8639f768ca3f75dbc4897f062b2e5200449cb9792f811cc7fc`  
		Last Modified: Tue, 30 Sep 2025 02:03:06 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268dcad5982db2c20530b19e5be820cb5fa032883dae77005422f9930a6b1a5e`  
		Last Modified: Tue, 30 Sep 2025 02:03:07 GMT  
		Size: 16.6 KB (16641 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:c49dc5f45776c0d100db5b086f6c54c23bd620d0e7543a159452354545a1e2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747d0bcf54a8c42e56b8cdd4d84f10cf70348637de5234c18b8ad0400ca88ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22faea7eae410e22e76d8d8ecf1e7479df19c2feca6920129c88123a2983c77b`  
		Last Modified: Tue, 30 Sep 2025 14:52:31 GMT  
		Size: 5.6 MB (5567126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75663d3a523baf385914288571496f152eda4d27fa6b8793f0d98df87a9e242`  
		Last Modified: Tue, 30 Sep 2025 14:52:37 GMT  
		Size: 177.4 MB (177412369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3e482aa54d18d1ecb2b8bb984385089d3d7905dbef00ed8be0626a86f54c8a`  
		Last Modified: Tue, 30 Sep 2025 00:40:38 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9297f47b0901ac1f0416670abc684a7f1da3d6d7261ef7e2344f1f5cf453ed78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9534bc50ebb2526afd67f835364914bf33db8f53791d2e9a2fc386102835ab73`

```dockerfile
```

-	Layers:
	-	`sha256:751bc869bb0837e2c3b7b4b37923b114bcc822c59715ac6bf16f7b47fac5328a`  
		Last Modified: Tue, 30 Sep 2025 02:03:11 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de3b3d4762f479d244698d0611be0f762d6b62df02a2790063590d769ba70a7`  
		Last Modified: Tue, 30 Sep 2025 02:03:12 GMT  
		Size: 16.7 KB (16736 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:d5178629204b5c199bdaf495ce91fc63c9ca35053bac4b400afe2b2e6dd02c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192895936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30d250ef264455e19c57e8a865a0a7e6670759cbd2c1e059650ae2d7276c75b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c05b711baf2fbb0ea28f1471b9c21eccfbd1afbc38f720524210adafa7cbf`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 5.9 MB (5878055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99b1bd6618c529345329aaef39117bbebb05c2a1b97d5b5e8af355b7ee2b77a`  
		Last Modified: Tue, 30 Sep 2025 20:22:46 GMT  
		Size: 157.8 MB (157807881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9927a86c8e920937918dad744f3a35b882c69d3af1dbe1e816a67fdabe983f`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9be026b01a496eb718b203f93742bce6d63cc1605e6fa920c4f7999ca54a9d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44456cac65eb6e4a40b596f12e071f09c3b31169d4a875f75f8c35731b45a003`

```dockerfile
```

-	Layers:
	-	`sha256:f35ae8c2a93ff712162de5397645e375fba332fadccad32202f18b06fbe709aa`  
		Last Modified: Tue, 30 Sep 2025 02:03:16 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238be5b9615499321f8af30e5715b8d2f49995f7b766c9a94e7081a432db0b57`  
		Last Modified: Tue, 30 Sep 2025 02:03:16 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:3c831cbfedc06f4fd17f396abb9bb1e323f9bae45253583be3e9210c645ea357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9830c8a7199b60f02e771383bb11cbd5c2fbbebaa9ee9f6907303dd29545352`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae5078f4b42d42980e7af775968ea12030fa58a473b5ada40edb06ba780153`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 6.3 MB (6256416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12db94eacc45cb74a1164c1edb5292200eaa5321ee2fa5e8b8d7ec2e31fa4ca9`  
		Last Modified: Tue, 30 Sep 2025 20:22:46 GMT  
		Size: 155.4 MB (155354786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9727d695276160cee404b93676a5ab642c5707cb4bef86f31283eca2a79f3795`  
		Last Modified: Mon, 29 Sep 2025 23:57:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5215cac9e887a1f245da35205d53118278161c0b4ff2dcc7f9497f9483b8633b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca60ac1a58d7cb1a4e3b17394190dbef116ab3cc67d63a50a6a9164de848c7c`

```dockerfile
```

-	Layers:
	-	`sha256:27637cae709f0f79bb0bf3c4f7ddd66d2d170533fdb50c094fea2d24594cc843`  
		Last Modified: Tue, 30 Sep 2025 02:03:20 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9dce671a122e86edda90327444044a49844a1803e15371bda704b0aa762589`  
		Last Modified: Tue, 30 Sep 2025 02:03:21 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-trixie`

```console
$ docker pull julia@sha256:49526ad6e28ba6129e3063100904c355b237ff47b73dadb476e0513f0a98575d
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
$ docker pull julia@sha256:9bdd2e8d822585ae438fef96106f4f82cccb703cd7ca945a4c99f628e4793b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cef3f3b8f858a875c7d5f98f69f7917a5fc6c69b46387946144032d99e9f487`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f707d58098b48b1282a096b0cc43a742bb413762e984b0d4977680d4ae12da6`  
		Last Modified: Mon, 29 Sep 2025 23:56:24 GMT  
		Size: 6.2 MB (6242822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0144b6cd8f232595608450312327d15baeaba8112806778d8500a106a30b877e`  
		Last Modified: Tue, 30 Sep 2025 03:00:15 GMT  
		Size: 176.4 MB (176362247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d54c2099e5a781a654e3d4e9fc78b69f251699777e1aa9fd27b3114c7bdcd1`  
		Last Modified: Mon, 29 Sep 2025 23:56:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5b92289408cd2e9634f67a8bb95ac0d8fec7feec820f5f4b46f34cdab481b989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3722500dab1d1bb74004e572577c52c339597f86ada79b8c9a40f77568fbb6`

```dockerfile
```

-	Layers:
	-	`sha256:b6582600941bd55bc9515a5b5d9c81c5ece79c072569fdbd5cdf02da4b0ee99c`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 2.2 MB (2240099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ffb549b8e93ab6069ddf4310cab2995edb4a47ef7b19ffed7985885f781df81`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 17.2 KB (17211 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ea2e89e2c68a1aa87cef5d58f6c6c4a9fd72dadde64dc65bf1f4c5d02cd7551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213744371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffef92cd6b6877ee5bb5648ba20a6bea4d4316d60861afd4969b716c87b70a10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24134d35066eccc57f1cfd9ea3628f2f0bd08dd14b257200d3f308d3cfa9649f`  
		Last Modified: Mon, 29 Sep 2025 23:56:29 GMT  
		Size: 6.2 MB (6153035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9b4bd31b16e44c7f444d0424964e663523aa2a6a9a67cb3e2580a1da979271`  
		Last Modified: Tue, 30 Sep 2025 11:48:58 GMT  
		Size: 177.5 MB (177450122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f85ef13ddde40c480fddcf7fe6f2fb64ea19c5ff25aa57216acd983a31ab2eb`  
		Last Modified: Mon, 29 Sep 2025 23:56:28 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:768330402ab6a5b7101096a6781bf79e0c79a220824fa0ddf8f26605e3513f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1807bf8b6bc8e2a448c1448f6b7fc33e99175be9147e7a95272d2ab74149e8b8`

```dockerfile
```

-	Layers:
	-	`sha256:a146189b1be62d10ecf4e2d4d0b421ff0b4532edb681c86d7c8bd97dca30ac75`  
		Last Modified: Tue, 30 Sep 2025 02:02:57 GMT  
		Size: 2.2 MB (2239149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb85f3f31926fa13b79f284fd226b9047ad4eb33cdf23a7c51725250d97e6f6`  
		Last Modified: Tue, 30 Sep 2025 02:02:58 GMT  
		Size: 17.3 KB (17330 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:ec57c259586605864e41423b8bda7fba131a10b0c655694d4f0e6ee19e71fc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb080987b44fe22f2d5fc329198b2f071fbdc168ab2a785b3412845dd12fb1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7653834ba0a8a0acd1b09ab2c5f73ea430d1c5ea9b14a623ae0dc9a67e567128`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30c835f063247ee20f910ca6b88d312a9262311f206a046418e14d7904433f1`  
		Last Modified: Tue, 30 Sep 2025 20:22:52 GMT  
		Size: 157.8 MB (157841832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97896db05c9a7c73c76f3699521152eccd99ec03d6afb9763eb702d22726b282`  
		Last Modified: Mon, 29 Sep 2025 23:56:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:5f86066e6ba7e263f7806760b4d95ff1bff5385fa55180e3ab55543cd3e79c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acb6318a864e3966d428b4e40272c2f9213b7befa20d17d8b1165d3ab321a6ae`

```dockerfile
```

-	Layers:
	-	`sha256:d42c2e787f2a387ce69818eb8d50469e94874c6b37f543dd9e0f04650a54e63a`  
		Last Modified: Tue, 30 Sep 2025 02:03:02 GMT  
		Size: 2.2 MB (2237244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bfa85468960b4c41127cd8ac60229fa3d681c7c036806068ad7ae688d74daab`  
		Last Modified: Tue, 30 Sep 2025 02:03:03 GMT  
		Size: 17.2 KB (17177 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:30d84856fd171760ce0a9862d1a33e552daaa338eb37c8f9baaa54f982bf39a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eddcb1f0f78a269edb3bbe11ca9baf096a3516c9746b72f91b3ca95475b8086`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 08 Aug 2025 17:33:54 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5e049a22458b36b2d3ea4032641756768b7a2948255b7d1190bc00cee73fa5`  
		Last Modified: Wed, 01 Oct 2025 19:50:16 GMT  
		Size: 155.4 MB (155388263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e7bc991b97ad3c3b076d2e166c04773f1f7eef81c48fd801f6c80e8e778a1`  
		Last Modified: Tue, 30 Sep 2025 06:59:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:92a5e8ad68115edc663db39f6f57857a37bf29c0d90a170c11329e0ff53129a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45b9005e68dbb4df1cccbad1ae0683c6efe0fd05282f13c292f6bbd7af9982b`

```dockerfile
```

-	Layers:
	-	`sha256:a8ae5b88e9b657ffd7db9a58e5fb73d94bd18ae5636fcf9bec841a59e7401680`  
		Last Modified: Wed, 01 Oct 2025 20:02:37 GMT  
		Size: 2.2 MB (2242594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72a22e7cf4697522c5969d96f8a3688f4cf6dd3860122004d29e476e8bcdfd3f`  
		Last Modified: Wed, 01 Oct 2025 20:02:38 GMT  
		Size: 17.3 KB (17257 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-windowsservercore`

```console
$ docker pull julia@sha256:28acbfc3b79a13146552c59a17f82fc89afcf2598f0c21327f361cf44068ec4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.10.10-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:da67cbb6230b4b9dcabb30a422c650d00461f556f32a1f3be39997471f37def3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3760210945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b1c0f868905a5338a67c399a13a5d62242912efac8938c789540dbac48b3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:36 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d87d05a897bccb5f2b7b0f22a2b7312f68dc3c05d98e93bd4b174511375fd`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9eaf5fcd45138239d877efa9dac052ec12bcacbc692aae3bef9bdacfe29c4`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa8b00aad4e24b567fd98cb2aae6e70687f65c9e58d30bbbc43ffbbd51066e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85846a480db99cf371627c3469d0766b75967b3d53e637cfaecd0d139873917d`  
		Last Modified: Wed, 10 Sep 2025 23:03:15 GMT  
		Size: 188.8 MB (188764648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dadd3c915b1707b2d227974d8bb0390fddf3d5d51303c0818a22048e0b6d7`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:be47fca4d707b05e29ce3ff64816d89d3804c3c57637f597808fa1da7bb2267b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470929970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2ef2f42509e55312e4a99a4f497a610248e3a544b25ac6181575751bd98b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:09 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:11 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e1324c130b59cc18854ac448cfe66bbdc6ea607d02d5a5efddbcbb3ccf199`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f6fdb153be7a554e4d0138b415168278f965f1a7ffe38c39dfd74aae2c5d2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc520230594198d2f30051a2544a775e109761bb519daa250651f7725fc796`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409404ed358ab10b3cdc090e5c12846484bec36fdd3bc479b22ae1b4c40797`  
		Last Modified: Wed, 10 Sep 2025 23:03:11 GMT  
		Size: 188.8 MB (188778455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06419495af2c922b2789cc1b07e6ddf74173cf1485fd4aa8f838f47f3552f1c2`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:5fd0a141c8fe1b45fdb1e320c793b7442c52ca7fd73d3d4acaedf587d6dc2fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1.10.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:be47fca4d707b05e29ce3ff64816d89d3804c3c57637f597808fa1da7bb2267b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2470929970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf2ef2f42509e55312e4a99a4f497a610248e3a544b25ac6181575751bd98b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:09 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:11 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9811425449e84dcbd33b2ae7b7f37c3b7fd53dcd7b0401fd37de5fddd1a09096`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e1324c130b59cc18854ac448cfe66bbdc6ea607d02d5a5efddbcbb3ccf199`  
		Last Modified: Wed, 10 Sep 2025 21:55:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f6fdb153be7a554e4d0138b415168278f965f1a7ffe38c39dfd74aae2c5d2a`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bc520230594198d2f30051a2544a775e109761bb519daa250651f7725fc796`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d409404ed358ab10b3cdc090e5c12846484bec36fdd3bc479b22ae1b4c40797`  
		Last Modified: Wed, 10 Sep 2025 23:03:11 GMT  
		Size: 188.8 MB (188778455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06419495af2c922b2789cc1b07e6ddf74173cf1485fd4aa8f838f47f3552f1c2`  
		Last Modified: Wed, 10 Sep 2025 21:55:59 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:6c18cb8bfa4a2f34a25e804b641c19183540d1b115f623bce3d3b8a6d96a7673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1.10.10-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:da67cbb6230b4b9dcabb30a422c650d00461f556f32a1f3be39997471f37def3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3760210945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b1c0f868905a5338a67c399a13a5d62242912efac8938c789540dbac48b3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_VERSION=1.10.10
# Wed, 10 Sep 2025 21:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Wed, 10 Sep 2025 21:49:36 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Wed, 10 Sep 2025 21:50:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:50:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fd427e102cbe35deefe716d425d4fb43161e3bb67a6a5fb81d622845645d2e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605d87d05a897bccb5f2b7b0f22a2b7312f68dc3c05d98e93bd4b174511375fd`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a9eaf5fcd45138239d877efa9dac052ec12bcacbc692aae3bef9bdacfe29c4`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaa8b00aad4e24b567fd98cb2aae6e70687f65c9e58d30bbbc43ffbbd51066e`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85846a480db99cf371627c3469d0766b75967b3d53e637cfaecd0d139873917d`  
		Last Modified: Wed, 10 Sep 2025 23:03:15 GMT  
		Size: 188.8 MB (188764648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dadd3c915b1707b2d227974d8bb0390fddf3d5d51303c0818a22048e0b6d7`  
		Last Modified: Wed, 10 Sep 2025 21:58:30 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:b95c5e7d5e2148a6385ba6bec4182f051cfd7970de5e367b8ca82cbf28a02f9f
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
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:326bc26fbd471c5d6a9ce3223b397f3a6ce82fdcf22c12959e9f89b4d7b3e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a504ff0e7a27b1cceb22fa1f05412ecaafe7eb60ca472ddd6630c00da228ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35198d700bd80bfc35ce8c55de7e701a51e8cb9f3803bf9df0d0c77ced13005a`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 6.2 MB (6242807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f1179db75e25c3d828377fa03ef5c43c6baabe1844b277a02cc6a13a6b1c6`  
		Last Modified: Tue, 30 Sep 2025 02:07:50 GMT  
		Size: 288.8 MB (288825564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73115d11584cfe84789fa07169b448634744355182e5b4188e1edbbfd5874641`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:f192d21f3596c6e0b3c269111bf684af8a469a0dfda5dd91b7b01cf448943203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b476b2c6991e32f89d9c9c6156843680e47496fd5db2d1aa4307f5d84a892269`

```dockerfile
```

-	Layers:
	-	`sha256:298f4cb9fc6582f6de4fe9bf44a467b6c3363acb2341d53dfecfc580c4fa5168`  
		Last Modified: Tue, 30 Sep 2025 02:02:24 GMT  
		Size: 2.2 MB (2240039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145038bd58d13db073742ec2d9f1ddd9c53a1ae7f786338124f7fa4b95c2f538`  
		Last Modified: Tue, 30 Sep 2025 02:02:25 GMT  
		Size: 18.4 KB (18370 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e49d83ec50115b76f98e40902bcdcde7d9dbd5b1369b0af2627dda65e188d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340967063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15e57ff5e164ac99b7f9a66bc36084d8f487638018dfe7f15157c5fc5d3902d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af16b2156c5cff3aed5dec9a2704c4ead2a130620eb96ddf912420acf560095`  
		Last Modified: Tue, 30 Sep 2025 06:58:42 GMT  
		Size: 6.2 MB (6153067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afa601e6e3b13448e72856bf7e01ed0b8704d565fb7f6bce4628a633fcbe55d`  
		Last Modified: Tue, 30 Sep 2025 06:59:02 GMT  
		Size: 304.7 MB (304672786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125a76383a76011d25f9c73edb44d70d308d1686317d69b1a7454c020590a523`  
		Last Modified: Tue, 30 Sep 2025 00:40:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:7116c5c64db39ee5c319dcdbfa227d0f175f7455081a973bb118c16adaec2f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0132cb21b633054468f15dba8685fa97491d4febca427d428152533cc0a5fb2`

```dockerfile
```

-	Layers:
	-	`sha256:a0afc47e6d71dc6c3791516f463297507f8e9395a289a067a8a51159c83f03e8`  
		Last Modified: Tue, 30 Sep 2025 02:02:28 GMT  
		Size: 2.2 MB (2240371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e5e1cf8bed8e62c59ca1eba5d7f1a5027feaf049713580c3afce55ffa83e1c`  
		Last Modified: Tue, 30 Sep 2025 02:02:29 GMT  
		Size: 18.5 KB (18539 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:78364e7c473818045e8faa5127d2775db950b6510d10f99d275f023cbceb6bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52902fea8856ccfd3489ec7eea27b16a8539b24faf39b22559b766a68f0d6735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf43d3f929850bc8b305964e38af47f28f6914812300f6d41f0c0566217d296`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86a1d8eebb14b18f95482b5fed7f7db921edb4a36923a1fa729a8ff9a51e60c`  
		Last Modified: Tue, 30 Sep 2025 20:26:06 GMT  
		Size: 237.6 MB (237589431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023959bd9272a6e302a2b0fb8896601ccdcd968a4a0a55cc328b342907b505a8`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:7296725d9ab598015ca98612df843236f5ad8e5927904e8e39149ecee557367a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ceb7ad92ad886a174b1c6d5f3ac1377b18e259d1d546188e0357f79a0b462f`

```dockerfile
```

-	Layers:
	-	`sha256:b9b6e117d660f20a6c91c880c4e66c91af9b349e29b30e3c9bff4e182715fd91`  
		Last Modified: Tue, 30 Sep 2025 02:02:33 GMT  
		Size: 2.2 MB (2237164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438071e2dc49ef212a56700c5088515884d11d48893d846ff0f95eb1129395d6`  
		Last Modified: Tue, 30 Sep 2025 02:02:34 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:5912f029cf4d6321609eb33edd16b4575a95e02133ad8f265aea647bc6106758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f94b0200351f6e3cbc79f6dfa221b3a8e7ed38e4eaecb69e1e2c1100f7c348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aff53bcbf0ccfa4a12e4dba0e15bb49d8680f56beb5cc7ccd42cd6457b378a8`  
		Last Modified: Wed, 01 Oct 2025 20:33:37 GMT  
		Size: 248.6 MB (248575957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4b71d712ca77414bef94e96e73dc8dc72bf2a2b989066359f0d2906731839`  
		Last Modified: Tue, 30 Sep 2025 06:57:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:47fec0456536af0001ea180916b0432a4bc6ac82253a6ddbe3fec286bebe8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e044ef29fabba4707cff9eac02801052116c43482dcfe92b47e18a4f00195ed`

```dockerfile
```

-	Layers:
	-	`sha256:5c88bb84b3dc2a651eabf5bb5fbfc4c918360e8227659dd36a5382a8c6bdcf9c`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2243792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183a871be75345d47a3f5a3fa6b872549f7110591f2e64b1aed193fc9a8505d8`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 18.4 KB (18442 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:ac38828597ed9bc945af1f4c4d588f85f3dd9846b6f8cb011a1a0cbd741a71c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3857533541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e33deb4d788a9bc8e0ff97d7533b9acb9fe5080668181f9c72c773d96fb2fb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 16 Sep 2025 17:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:35:33 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:35:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:35:35 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:37:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:37:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742bac5f17e737de033ac777c204f1da3eaed901a8ab4824de82bddcb635f97`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76f7fb7bd665fc8faa00d7204a8760a0db2c5299d75e53d32beb09a7095c13a`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081524dee08f1cf8f958c8175ede4627342d6e474edfaaef65e5a7d3090a0ad`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197bcfee6f005fecea1c486189f5d490e414368b3f87c57e104e54c1f55f2e8d`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50561f1b5d3a6703b4542e900ae8cd5e04398a6ea9797d662272ab7ed952d1`  
		Last Modified: Tue, 16 Sep 2025 20:03:22 GMT  
		Size: 286.1 MB (286087265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96a781c701973f728528c3ed6085d8cd7747d1bcb783559181b3bda9e6878`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:4ecd2ef8c4f890f85b0c8c26e46bc9d6888e96f921034b131e8addd69443ab3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568142462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8ca6e16146fedaef00cd44d27ace88bb27eb06350fe87df9be881480133657`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 16 Sep 2025 17:26:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:26:50 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:28:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da14a5aec402a0258fb230e5287bd5c53cb7fb91a9da0beac007e12b1521a9e`  
		Last Modified: Tue, 16 Sep 2025 17:28:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0d4d7fec49929952b1b90327e5f276863c5a95c0fe43f75843eb46e0953683`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc98f37b821fa6fa2d39022f2edd7ee706fb98375d308b9f6a9c8c9656e9e`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc28737c5b2f8a60d5b2ad12cff93a80cb1e8b281a83903d33fb781c18802`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b745b8cf856d2e683248255707cd8effb563b362c6b8bf774427905284459906`  
		Last Modified: Tue, 16 Sep 2025 20:03:45 GMT  
		Size: 286.0 MB (285990940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815888fad5b56125ed2f55bc222bf9674af3c17ecc01a775aaed551d174baae2`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:298802749e0003caa5874d80255bc31699785117c5facb752e9d60d794349a1d
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
$ docker pull julia@sha256:2886ea9ee3c46ff842cc0630b1722ad8e292d8ab8c84af4e6319336c2874a083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5a24508cd364f9da0a7d28de9f69755c87ce9ab24279127da6c72f28e5c4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8918b81ad197821e453c6dcb53a7c99da35892309ad513e8a8479a91b4a2803`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 5.7 MB (5716270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51416d23c5135be08ace3a60d9ce7d959e2a3de29512435d10fa4d0b0e5605d`  
		Last Modified: Tue, 30 Sep 2025 15:52:41 GMT  
		Size: 288.8 MB (288788389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75452265d29af360b7b778ddc6ff9cdb8d6667a0b263880d724266fb24d48f44`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:dec4c638a7ba4a2a56c01ebb1ee173fe8d32137ec3f8f257be75e1b3e697e4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d4c434db8f726207c1756c94319a0f70b78e4cb93fce817914ebe4c9f6864`

```dockerfile
```

-	Layers:
	-	`sha256:43ca1e405ad96739ee5accf6cb51682b8d377a6072e08199a828541e483ed68a`  
		Last Modified: Tue, 30 Sep 2025 02:02:38 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990221cc4a3e1dee3f3288eaaee9733efebc7f2470a740a1df2cb995e937b8c7`  
		Last Modified: Tue, 30 Sep 2025 02:02:39 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6c5e13fc5db26248d10c44e111d84752b6ce09d40e9a92d724b20fd1175a1740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579824868583c4bd1415d07e78e6b69178bb88294adaa39d4b44f8fea70936d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a29ff6845aa7a1c72549e3a1249be4087e98bd381d7964e05f0bf1e99117eb0`  
		Last Modified: Mon, 29 Sep 2025 23:57:03 GMT  
		Size: 5.6 MB (5567126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c52275ced3e56c7b3b87d8256a541f9f384ed0955ed3fc9e3f1bafd63d3011`  
		Last Modified: Tue, 30 Sep 2025 20:24:19 GMT  
		Size: 304.6 MB (304646640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7885859e7e712221d373d9ebbd78faf3814ab37bcf33fb391082c1c677737aba`  
		Last Modified: Mon, 29 Sep 2025 23:57:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:422eb4380b846ca127559aee5f10468b09852a6b33095226dbe693bf9d323986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ab1de9c0aec566234a7c3b17c11ff4f0552339f1d381192ae66edaf2f677cf`

```dockerfile
```

-	Layers:
	-	`sha256:dcafd7af4d13e8fd340636692df4e8c9c4a8189f7647ffe0daa5a49147cd5baf`  
		Last Modified: Tue, 30 Sep 2025 02:02:43 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c140c3d8b337ed216c9c2925c1e02ff6b9515c554874e4b0959e68f63433c3f8`  
		Last Modified: Tue, 30 Sep 2025 02:02:44 GMT  
		Size: 17.3 KB (17348 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b80f5c8f7494ce7e898fff7028d3855e6965d6d64a4c2c3d91fd89cca0311faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4e93dc9c13249f4ede7fbadf95201b4e06323d79ff3df68136a1a907218a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e566c0658944f0601bbdb7b62a9cdcbe1eb595ac355d8611c40149b8b31a5677`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 5.9 MB (5878038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aad7c79b5a267fc4087390aaa1afe060d7373393c375f7a6f9fd1168f048bd`  
		Last Modified: Tue, 30 Sep 2025 20:15:27 GMT  
		Size: 237.6 MB (237555777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bb2b42f455b001274014ecd7b7c5d0a707d7e6923396ac082e344b2e5117ba`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0877d54c5cfb5810d74a04379a224f3f210a37f64d6c55b7cc489ec0085137d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa694e1b59f269b5503493d82526640fd74bc5cc8b0a6d433b7d74fa410822f`

```dockerfile
```

-	Layers:
	-	`sha256:84be3b85dcc4a6297c192ee4a46d681cfe33bf8ab67dfcacccc5853c0e31a1c7`  
		Last Modified: Tue, 30 Sep 2025 02:02:47 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df8213edcaad1e51cbc7878ec0f418b5126936fed00e1620aab8d2dccb12377`  
		Last Modified: Tue, 30 Sep 2025 02:02:48 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:640536e02ea69be1f6d719a08a3ff00c4f639e5b90f2a30fa158b126025a1cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f97bd1ee1470efc9d53bece09428538b4601d02e59c5b11f387cea2899e4726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae5078f4b42d42980e7af775968ea12030fa58a473b5ada40edb06ba780153`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 6.3 MB (6256416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee5310e8e3fd3580beefbf87c369f5521121e85a63567811972d0742f8b078`  
		Last Modified: Tue, 30 Sep 2025 20:23:05 GMT  
		Size: 248.6 MB (248553901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7f04345b65168ad8224f68cdcddac193f7431d000391ea476004285be9ddd8`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e343180a144055db82c20cc4b4840f86597c9ec5e6586dd0bb4ba65dde121553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d3f180bdfa35a5115d1269ab44c8a7e49008996f48b8b30a6babb1bb82cba2`

```dockerfile
```

-	Layers:
	-	`sha256:2be392bd50454bb050c37762204bba99ce43d2653f79557db404d11748a873dc`  
		Last Modified: Tue, 30 Sep 2025 02:02:52 GMT  
		Size: 2.6 MB (2572214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1b4954811dce39d3f3f01514a001f8455f7aa3cbda64b340c3dfa632bdc6ea`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 17.3 KB (17272 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-trixie`

```console
$ docker pull julia@sha256:3afc2d24ee9b2e4f507f58210df68d413b2df513e0c646fbdd7c15c2840a1aec
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
$ docker pull julia@sha256:326bc26fbd471c5d6a9ce3223b397f3a6ce82fdcf22c12959e9f89b4d7b3e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a504ff0e7a27b1cceb22fa1f05412ecaafe7eb60ca472ddd6630c00da228ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35198d700bd80bfc35ce8c55de7e701a51e8cb9f3803bf9df0d0c77ced13005a`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 6.2 MB (6242807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f1179db75e25c3d828377fa03ef5c43c6baabe1844b277a02cc6a13a6b1c6`  
		Last Modified: Tue, 30 Sep 2025 02:07:50 GMT  
		Size: 288.8 MB (288825564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73115d11584cfe84789fa07169b448634744355182e5b4188e1edbbfd5874641`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f192d21f3596c6e0b3c269111bf684af8a469a0dfda5dd91b7b01cf448943203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b476b2c6991e32f89d9c9c6156843680e47496fd5db2d1aa4307f5d84a892269`

```dockerfile
```

-	Layers:
	-	`sha256:298f4cb9fc6582f6de4fe9bf44a467b6c3363acb2341d53dfecfc580c4fa5168`  
		Last Modified: Tue, 30 Sep 2025 02:02:24 GMT  
		Size: 2.2 MB (2240039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145038bd58d13db073742ec2d9f1ddd9c53a1ae7f786338124f7fa4b95c2f538`  
		Last Modified: Tue, 30 Sep 2025 02:02:25 GMT  
		Size: 18.4 KB (18370 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e49d83ec50115b76f98e40902bcdcde7d9dbd5b1369b0af2627dda65e188d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340967063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15e57ff5e164ac99b7f9a66bc36084d8f487638018dfe7f15157c5fc5d3902d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af16b2156c5cff3aed5dec9a2704c4ead2a130620eb96ddf912420acf560095`  
		Last Modified: Tue, 30 Sep 2025 06:58:42 GMT  
		Size: 6.2 MB (6153067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afa601e6e3b13448e72856bf7e01ed0b8704d565fb7f6bce4628a633fcbe55d`  
		Last Modified: Tue, 30 Sep 2025 06:59:02 GMT  
		Size: 304.7 MB (304672786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125a76383a76011d25f9c73edb44d70d308d1686317d69b1a7454c020590a523`  
		Last Modified: Tue, 30 Sep 2025 00:40:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7116c5c64db39ee5c319dcdbfa227d0f175f7455081a973bb118c16adaec2f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0132cb21b633054468f15dba8685fa97491d4febca427d428152533cc0a5fb2`

```dockerfile
```

-	Layers:
	-	`sha256:a0afc47e6d71dc6c3791516f463297507f8e9395a289a067a8a51159c83f03e8`  
		Last Modified: Tue, 30 Sep 2025 02:02:28 GMT  
		Size: 2.2 MB (2240371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e5e1cf8bed8e62c59ca1eba5d7f1a5027feaf049713580c3afce55ffa83e1c`  
		Last Modified: Tue, 30 Sep 2025 02:02:29 GMT  
		Size: 18.5 KB (18539 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; 386

```console
$ docker pull julia@sha256:78364e7c473818045e8faa5127d2775db950b6510d10f99d275f023cbceb6bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52902fea8856ccfd3489ec7eea27b16a8539b24faf39b22559b766a68f0d6735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf43d3f929850bc8b305964e38af47f28f6914812300f6d41f0c0566217d296`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86a1d8eebb14b18f95482b5fed7f7db921edb4a36923a1fa729a8ff9a51e60c`  
		Last Modified: Tue, 30 Sep 2025 20:26:06 GMT  
		Size: 237.6 MB (237589431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023959bd9272a6e302a2b0fb8896601ccdcd968a4a0a55cc328b342907b505a8`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7296725d9ab598015ca98612df843236f5ad8e5927904e8e39149ecee557367a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ceb7ad92ad886a174b1c6d5f3ac1377b18e259d1d546188e0357f79a0b462f`

```dockerfile
```

-	Layers:
	-	`sha256:b9b6e117d660f20a6c91c880c4e66c91af9b349e29b30e3c9bff4e182715fd91`  
		Last Modified: Tue, 30 Sep 2025 02:02:33 GMT  
		Size: 2.2 MB (2237164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438071e2dc49ef212a56700c5088515884d11d48893d846ff0f95eb1129395d6`  
		Last Modified: Tue, 30 Sep 2025 02:02:34 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:5912f029cf4d6321609eb33edd16b4575a95e02133ad8f265aea647bc6106758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f94b0200351f6e3cbc79f6dfa221b3a8e7ed38e4eaecb69e1e2c1100f7c348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aff53bcbf0ccfa4a12e4dba0e15bb49d8680f56beb5cc7ccd42cd6457b378a8`  
		Last Modified: Wed, 01 Oct 2025 20:33:37 GMT  
		Size: 248.6 MB (248575957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4b71d712ca77414bef94e96e73dc8dc72bf2a2b989066359f0d2906731839`  
		Last Modified: Tue, 30 Sep 2025 06:57:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:47fec0456536af0001ea180916b0432a4bc6ac82253a6ddbe3fec286bebe8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e044ef29fabba4707cff9eac02801052116c43482dcfe92b47e18a4f00195ed`

```dockerfile
```

-	Layers:
	-	`sha256:5c88bb84b3dc2a651eabf5bb5fbfc4c918360e8227659dd36a5382a8c6bdcf9c`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2243792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183a871be75345d47a3f5a3fa6b872549f7110591f2e64b1aed193fc9a8505d8`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 18.4 KB (18442 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:8a3401a95c02b86a61976194f946720c8a71e4ac3f104b78089d02b3004f3d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:ac38828597ed9bc945af1f4c4d588f85f3dd9846b6f8cb011a1a0cbd741a71c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3857533541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e33deb4d788a9bc8e0ff97d7533b9acb9fe5080668181f9c72c773d96fb2fb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 16 Sep 2025 17:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:35:33 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:35:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:35:35 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:37:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:37:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742bac5f17e737de033ac777c204f1da3eaed901a8ab4824de82bddcb635f97`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76f7fb7bd665fc8faa00d7204a8760a0db2c5299d75e53d32beb09a7095c13a`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081524dee08f1cf8f958c8175ede4627342d6e474edfaaef65e5a7d3090a0ad`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197bcfee6f005fecea1c486189f5d490e414368b3f87c57e104e54c1f55f2e8d`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50561f1b5d3a6703b4542e900ae8cd5e04398a6ea9797d662272ab7ed952d1`  
		Last Modified: Tue, 16 Sep 2025 20:03:22 GMT  
		Size: 286.1 MB (286087265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96a781c701973f728528c3ed6085d8cd7747d1bcb783559181b3bda9e6878`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:4ecd2ef8c4f890f85b0c8c26e46bc9d6888e96f921034b131e8addd69443ab3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568142462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8ca6e16146fedaef00cd44d27ace88bb27eb06350fe87df9be881480133657`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 16 Sep 2025 17:26:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:26:50 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:28:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da14a5aec402a0258fb230e5287bd5c53cb7fb91a9da0beac007e12b1521a9e`  
		Last Modified: Tue, 16 Sep 2025 17:28:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0d4d7fec49929952b1b90327e5f276863c5a95c0fe43f75843eb46e0953683`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc98f37b821fa6fa2d39022f2edd7ee706fb98375d308b9f6a9c8c9656e9e`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc28737c5b2f8a60d5b2ad12cff93a80cb1e8b281a83903d33fb781c18802`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b745b8cf856d2e683248255707cd8effb563b362c6b8bf774427905284459906`  
		Last Modified: Tue, 16 Sep 2025 20:03:45 GMT  
		Size: 286.0 MB (285990940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815888fad5b56125ed2f55bc222bf9674af3c17ecc01a775aaed551d174baae2`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:a0e25784c6fc13b850e0a7f6f69372ad1a91862652141185ff5ca4a538ba5910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:4ecd2ef8c4f890f85b0c8c26e46bc9d6888e96f921034b131e8addd69443ab3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568142462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8ca6e16146fedaef00cd44d27ace88bb27eb06350fe87df9be881480133657`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 16 Sep 2025 17:26:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:26:50 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:28:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da14a5aec402a0258fb230e5287bd5c53cb7fb91a9da0beac007e12b1521a9e`  
		Last Modified: Tue, 16 Sep 2025 17:28:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0d4d7fec49929952b1b90327e5f276863c5a95c0fe43f75843eb46e0953683`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc98f37b821fa6fa2d39022f2edd7ee706fb98375d308b9f6a9c8c9656e9e`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc28737c5b2f8a60d5b2ad12cff93a80cb1e8b281a83903d33fb781c18802`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b745b8cf856d2e683248255707cd8effb563b362c6b8bf774427905284459906`  
		Last Modified: Tue, 16 Sep 2025 20:03:45 GMT  
		Size: 286.0 MB (285990940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815888fad5b56125ed2f55bc222bf9674af3c17ecc01a775aaed551d174baae2`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fc177cf1115dd82b4737d48635b23655e9ccae982714ccaff769924ba6b962bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:ac38828597ed9bc945af1f4c4d588f85f3dd9846b6f8cb011a1a0cbd741a71c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3857533541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e33deb4d788a9bc8e0ff97d7533b9acb9fe5080668181f9c72c773d96fb2fb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 16 Sep 2025 17:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:35:33 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:35:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:35:35 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:37:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:37:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742bac5f17e737de033ac777c204f1da3eaed901a8ab4824de82bddcb635f97`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76f7fb7bd665fc8faa00d7204a8760a0db2c5299d75e53d32beb09a7095c13a`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081524dee08f1cf8f958c8175ede4627342d6e474edfaaef65e5a7d3090a0ad`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197bcfee6f005fecea1c486189f5d490e414368b3f87c57e104e54c1f55f2e8d`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50561f1b5d3a6703b4542e900ae8cd5e04398a6ea9797d662272ab7ed952d1`  
		Last Modified: Tue, 16 Sep 2025 20:03:22 GMT  
		Size: 286.1 MB (286087265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96a781c701973f728528c3ed6085d8cd7747d1bcb783559181b3bda9e6878`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7`

```console
$ docker pull julia@sha256:b95c5e7d5e2148a6385ba6bec4182f051cfd7970de5e367b8ca82cbf28a02f9f
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
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.11.7` - linux; amd64

```console
$ docker pull julia@sha256:326bc26fbd471c5d6a9ce3223b397f3a6ce82fdcf22c12959e9f89b4d7b3e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a504ff0e7a27b1cceb22fa1f05412ecaafe7eb60ca472ddd6630c00da228ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35198d700bd80bfc35ce8c55de7e701a51e8cb9f3803bf9df0d0c77ced13005a`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 6.2 MB (6242807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f1179db75e25c3d828377fa03ef5c43c6baabe1844b277a02cc6a13a6b1c6`  
		Last Modified: Tue, 30 Sep 2025 02:07:50 GMT  
		Size: 288.8 MB (288825564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73115d11584cfe84789fa07169b448634744355182e5b4188e1edbbfd5874641`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:f192d21f3596c6e0b3c269111bf684af8a469a0dfda5dd91b7b01cf448943203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b476b2c6991e32f89d9c9c6156843680e47496fd5db2d1aa4307f5d84a892269`

```dockerfile
```

-	Layers:
	-	`sha256:298f4cb9fc6582f6de4fe9bf44a467b6c3363acb2341d53dfecfc580c4fa5168`  
		Last Modified: Tue, 30 Sep 2025 02:02:24 GMT  
		Size: 2.2 MB (2240039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145038bd58d13db073742ec2d9f1ddd9c53a1ae7f786338124f7fa4b95c2f538`  
		Last Modified: Tue, 30 Sep 2025 02:02:25 GMT  
		Size: 18.4 KB (18370 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e49d83ec50115b76f98e40902bcdcde7d9dbd5b1369b0af2627dda65e188d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340967063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15e57ff5e164ac99b7f9a66bc36084d8f487638018dfe7f15157c5fc5d3902d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af16b2156c5cff3aed5dec9a2704c4ead2a130620eb96ddf912420acf560095`  
		Last Modified: Tue, 30 Sep 2025 06:58:42 GMT  
		Size: 6.2 MB (6153067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afa601e6e3b13448e72856bf7e01ed0b8704d565fb7f6bce4628a633fcbe55d`  
		Last Modified: Tue, 30 Sep 2025 06:59:02 GMT  
		Size: 304.7 MB (304672786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125a76383a76011d25f9c73edb44d70d308d1686317d69b1a7454c020590a523`  
		Last Modified: Tue, 30 Sep 2025 00:40:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:7116c5c64db39ee5c319dcdbfa227d0f175f7455081a973bb118c16adaec2f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0132cb21b633054468f15dba8685fa97491d4febca427d428152533cc0a5fb2`

```dockerfile
```

-	Layers:
	-	`sha256:a0afc47e6d71dc6c3791516f463297507f8e9395a289a067a8a51159c83f03e8`  
		Last Modified: Tue, 30 Sep 2025 02:02:28 GMT  
		Size: 2.2 MB (2240371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e5e1cf8bed8e62c59ca1eba5d7f1a5027feaf049713580c3afce55ffa83e1c`  
		Last Modified: Tue, 30 Sep 2025 02:02:29 GMT  
		Size: 18.5 KB (18539 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; 386

```console
$ docker pull julia@sha256:78364e7c473818045e8faa5127d2775db950b6510d10f99d275f023cbceb6bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52902fea8856ccfd3489ec7eea27b16a8539b24faf39b22559b766a68f0d6735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf43d3f929850bc8b305964e38af47f28f6914812300f6d41f0c0566217d296`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86a1d8eebb14b18f95482b5fed7f7db921edb4a36923a1fa729a8ff9a51e60c`  
		Last Modified: Tue, 30 Sep 2025 20:26:06 GMT  
		Size: 237.6 MB (237589431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023959bd9272a6e302a2b0fb8896601ccdcd968a4a0a55cc328b342907b505a8`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:7296725d9ab598015ca98612df843236f5ad8e5927904e8e39149ecee557367a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ceb7ad92ad886a174b1c6d5f3ac1377b18e259d1d546188e0357f79a0b462f`

```dockerfile
```

-	Layers:
	-	`sha256:b9b6e117d660f20a6c91c880c4e66c91af9b349e29b30e3c9bff4e182715fd91`  
		Last Modified: Tue, 30 Sep 2025 02:02:33 GMT  
		Size: 2.2 MB (2237164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438071e2dc49ef212a56700c5088515884d11d48893d846ff0f95eb1129395d6`  
		Last Modified: Tue, 30 Sep 2025 02:02:34 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; ppc64le

```console
$ docker pull julia@sha256:5912f029cf4d6321609eb33edd16b4575a95e02133ad8f265aea647bc6106758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f94b0200351f6e3cbc79f6dfa221b3a8e7ed38e4eaecb69e1e2c1100f7c348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aff53bcbf0ccfa4a12e4dba0e15bb49d8680f56beb5cc7ccd42cd6457b378a8`  
		Last Modified: Wed, 01 Oct 2025 20:33:37 GMT  
		Size: 248.6 MB (248575957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4b71d712ca77414bef94e96e73dc8dc72bf2a2b989066359f0d2906731839`  
		Last Modified: Tue, 30 Sep 2025 06:57:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:47fec0456536af0001ea180916b0432a4bc6ac82253a6ddbe3fec286bebe8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e044ef29fabba4707cff9eac02801052116c43482dcfe92b47e18a4f00195ed`

```dockerfile
```

-	Layers:
	-	`sha256:5c88bb84b3dc2a651eabf5bb5fbfc4c918360e8227659dd36a5382a8c6bdcf9c`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2243792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183a871be75345d47a3f5a3fa6b872549f7110591f2e64b1aed193fc9a8505d8`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 18.4 KB (18442 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:ac38828597ed9bc945af1f4c4d588f85f3dd9846b6f8cb011a1a0cbd741a71c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3857533541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e33deb4d788a9bc8e0ff97d7533b9acb9fe5080668181f9c72c773d96fb2fb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 16 Sep 2025 17:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:35:33 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:35:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:35:35 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:37:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:37:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742bac5f17e737de033ac777c204f1da3eaed901a8ab4824de82bddcb635f97`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76f7fb7bd665fc8faa00d7204a8760a0db2c5299d75e53d32beb09a7095c13a`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081524dee08f1cf8f958c8175ede4627342d6e474edfaaef65e5a7d3090a0ad`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197bcfee6f005fecea1c486189f5d490e414368b3f87c57e104e54c1f55f2e8d`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50561f1b5d3a6703b4542e900ae8cd5e04398a6ea9797d662272ab7ed952d1`  
		Last Modified: Tue, 16 Sep 2025 20:03:22 GMT  
		Size: 286.1 MB (286087265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96a781c701973f728528c3ed6085d8cd7747d1bcb783559181b3bda9e6878`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:4ecd2ef8c4f890f85b0c8c26e46bc9d6888e96f921034b131e8addd69443ab3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568142462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8ca6e16146fedaef00cd44d27ace88bb27eb06350fe87df9be881480133657`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 16 Sep 2025 17:26:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:26:50 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:28:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da14a5aec402a0258fb230e5287bd5c53cb7fb91a9da0beac007e12b1521a9e`  
		Last Modified: Tue, 16 Sep 2025 17:28:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0d4d7fec49929952b1b90327e5f276863c5a95c0fe43f75843eb46e0953683`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc98f37b821fa6fa2d39022f2edd7ee706fb98375d308b9f6a9c8c9656e9e`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc28737c5b2f8a60d5b2ad12cff93a80cb1e8b281a83903d33fb781c18802`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b745b8cf856d2e683248255707cd8effb563b362c6b8bf774427905284459906`  
		Last Modified: Tue, 16 Sep 2025 20:03:45 GMT  
		Size: 286.0 MB (285990940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815888fad5b56125ed2f55bc222bf9674af3c17ecc01a775aaed551d174baae2`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-bookworm`

```console
$ docker pull julia@sha256:298802749e0003caa5874d80255bc31699785117c5facb752e9d60d794349a1d
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
$ docker pull julia@sha256:2886ea9ee3c46ff842cc0630b1722ad8e292d8ab8c84af4e6319336c2874a083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5a24508cd364f9da0a7d28de9f69755c87ce9ab24279127da6c72f28e5c4ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8918b81ad197821e453c6dcb53a7c99da35892309ad513e8a8479a91b4a2803`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 5.7 MB (5716270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51416d23c5135be08ace3a60d9ce7d959e2a3de29512435d10fa4d0b0e5605d`  
		Last Modified: Tue, 30 Sep 2025 15:52:41 GMT  
		Size: 288.8 MB (288788389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75452265d29af360b7b778ddc6ff9cdb8d6667a0b263880d724266fb24d48f44`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:dec4c638a7ba4a2a56c01ebb1ee173fe8d32137ec3f8f257be75e1b3e697e4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7d4c434db8f726207c1756c94319a0f70b78e4cb93fce817914ebe4c9f6864`

```dockerfile
```

-	Layers:
	-	`sha256:43ca1e405ad96739ee5accf6cb51682b8d377a6072e08199a828541e483ed68a`  
		Last Modified: Tue, 30 Sep 2025 02:02:38 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990221cc4a3e1dee3f3288eaaee9733efebc7f2470a740a1df2cb995e937b8c7`  
		Last Modified: Tue, 30 Sep 2025 02:02:39 GMT  
		Size: 17.2 KB (17229 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6c5e13fc5db26248d10c44e111d84752b6ce09d40e9a92d724b20fd1175a1740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579824868583c4bd1415d07e78e6b69178bb88294adaa39d4b44f8fea70936d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a29ff6845aa7a1c72549e3a1249be4087e98bd381d7964e05f0bf1e99117eb0`  
		Last Modified: Mon, 29 Sep 2025 23:57:03 GMT  
		Size: 5.6 MB (5567126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c52275ced3e56c7b3b87d8256a541f9f384ed0955ed3fc9e3f1bafd63d3011`  
		Last Modified: Tue, 30 Sep 2025 20:24:19 GMT  
		Size: 304.6 MB (304646640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7885859e7e712221d373d9ebbd78faf3814ab37bcf33fb391082c1c677737aba`  
		Last Modified: Mon, 29 Sep 2025 23:57:02 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:422eb4380b846ca127559aee5f10468b09852a6b33095226dbe693bf9d323986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2585309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ab1de9c0aec566234a7c3b17c11ff4f0552339f1d381192ae66edaf2f677cf`

```dockerfile
```

-	Layers:
	-	`sha256:dcafd7af4d13e8fd340636692df4e8c9c4a8189f7647ffe0daa5a49147cd5baf`  
		Last Modified: Tue, 30 Sep 2025 02:02:43 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c140c3d8b337ed216c9c2925c1e02ff6b9515c554874e4b0959e68f63433c3f8`  
		Last Modified: Tue, 30 Sep 2025 02:02:44 GMT  
		Size: 17.3 KB (17348 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b80f5c8f7494ce7e898fff7028d3855e6965d6d64a4c2c3d91fd89cca0311faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272643810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4e93dc9c13249f4ede7fbadf95201b4e06323d79ff3df68136a1a907218a4b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e566c0658944f0601bbdb7b62a9cdcbe1eb595ac355d8611c40149b8b31a5677`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 5.9 MB (5878038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6aad7c79b5a267fc4087390aaa1afe060d7373393c375f7a6f9fd1168f048bd`  
		Last Modified: Tue, 30 Sep 2025 20:15:27 GMT  
		Size: 237.6 MB (237555777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bb2b42f455b001274014ecd7b7c5d0a707d7e6923396ac082e344b2e5117ba`  
		Last Modified: Mon, 29 Sep 2025 23:56:08 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0877d54c5cfb5810d74a04379a224f3f210a37f64d6c55b7cc489ec0085137d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa694e1b59f269b5503493d82526640fd74bc5cc8b0a6d433b7d74fa410822f`

```dockerfile
```

-	Layers:
	-	`sha256:84be3b85dcc4a6297c192ee4a46d681cfe33bf8ab67dfcacccc5853c0e31a1c7`  
		Last Modified: Tue, 30 Sep 2025 02:02:47 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df8213edcaad1e51cbc7878ec0f418b5126936fed00e1620aab8d2dccb12377`  
		Last Modified: Tue, 30 Sep 2025 02:02:48 GMT  
		Size: 17.2 KB (17196 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:640536e02ea69be1f6d719a08a3ff00c4f639e5b90f2a30fa158b126025a1cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f97bd1ee1470efc9d53bece09428538b4601d02e59c5b11f387cea2899e4726`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae5078f4b42d42980e7af775968ea12030fa58a473b5ada40edb06ba780153`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 6.3 MB (6256416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee5310e8e3fd3580beefbf87c369f5521121e85a63567811972d0742f8b078`  
		Last Modified: Tue, 30 Sep 2025 20:23:05 GMT  
		Size: 248.6 MB (248553901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7f04345b65168ad8224f68cdcddac193f7431d000391ea476004285be9ddd8`  
		Last Modified: Mon, 29 Sep 2025 23:55:14 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:e343180a144055db82c20cc4b4840f86597c9ec5e6586dd0bb4ba65dde121553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2589486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d3f180bdfa35a5115d1269ab44c8a7e49008996f48b8b30a6babb1bb82cba2`

```dockerfile
```

-	Layers:
	-	`sha256:2be392bd50454bb050c37762204bba99ce43d2653f79557db404d11748a873dc`  
		Last Modified: Tue, 30 Sep 2025 02:02:52 GMT  
		Size: 2.6 MB (2572214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa1b4954811dce39d3f3f01514a001f8455f7aa3cbda64b340c3dfa632bdc6ea`  
		Last Modified: Tue, 30 Sep 2025 02:02:53 GMT  
		Size: 17.3 KB (17272 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-trixie`

```console
$ docker pull julia@sha256:3afc2d24ee9b2e4f507f58210df68d413b2df513e0c646fbdd7c15c2840a1aec
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
$ docker pull julia@sha256:326bc26fbd471c5d6a9ce3223b397f3a6ce82fdcf22c12959e9f89b4d7b3e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a504ff0e7a27b1cceb22fa1f05412ecaafe7eb60ca472ddd6630c00da228ee17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35198d700bd80bfc35ce8c55de7e701a51e8cb9f3803bf9df0d0c77ced13005a`  
		Last Modified: Mon, 29 Sep 2025 23:56:05 GMT  
		Size: 6.2 MB (6242807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95f1179db75e25c3d828377fa03ef5c43c6baabe1844b277a02cc6a13a6b1c6`  
		Last Modified: Tue, 30 Sep 2025 02:07:50 GMT  
		Size: 288.8 MB (288825564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73115d11584cfe84789fa07169b448634744355182e5b4188e1edbbfd5874641`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f192d21f3596c6e0b3c269111bf684af8a469a0dfda5dd91b7b01cf448943203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b476b2c6991e32f89d9c9c6156843680e47496fd5db2d1aa4307f5d84a892269`

```dockerfile
```

-	Layers:
	-	`sha256:298f4cb9fc6582f6de4fe9bf44a467b6c3363acb2341d53dfecfc580c4fa5168`  
		Last Modified: Tue, 30 Sep 2025 02:02:24 GMT  
		Size: 2.2 MB (2240039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145038bd58d13db073742ec2d9f1ddd9c53a1ae7f786338124f7fa4b95c2f538`  
		Last Modified: Tue, 30 Sep 2025 02:02:25 GMT  
		Size: 18.4 KB (18370 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e49d83ec50115b76f98e40902bcdcde7d9dbd5b1369b0af2627dda65e188d0b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340967063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15e57ff5e164ac99b7f9a66bc36084d8f487638018dfe7f15157c5fc5d3902d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af16b2156c5cff3aed5dec9a2704c4ead2a130620eb96ddf912420acf560095`  
		Last Modified: Tue, 30 Sep 2025 06:58:42 GMT  
		Size: 6.2 MB (6153067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afa601e6e3b13448e72856bf7e01ed0b8704d565fb7f6bce4628a633fcbe55d`  
		Last Modified: Tue, 30 Sep 2025 06:59:02 GMT  
		Size: 304.7 MB (304672786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125a76383a76011d25f9c73edb44d70d308d1686317d69b1a7454c020590a523`  
		Last Modified: Tue, 30 Sep 2025 00:40:19 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7116c5c64db39ee5c319dcdbfa227d0f175f7455081a973bb118c16adaec2f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0132cb21b633054468f15dba8685fa97491d4febca427d428152533cc0a5fb2`

```dockerfile
```

-	Layers:
	-	`sha256:a0afc47e6d71dc6c3791516f463297507f8e9395a289a067a8a51159c83f03e8`  
		Last Modified: Tue, 30 Sep 2025 02:02:28 GMT  
		Size: 2.2 MB (2240371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e5e1cf8bed8e62c59ca1eba5d7f1a5027feaf049713580c3afce55ffa83e1c`  
		Last Modified: Tue, 30 Sep 2025 02:02:29 GMT  
		Size: 18.5 KB (18539 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; 386

```console
$ docker pull julia@sha256:78364e7c473818045e8faa5127d2775db950b6510d10f99d275f023cbceb6bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52902fea8856ccfd3489ec7eea27b16a8539b24faf39b22559b766a68f0d6735`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
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
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf43d3f929850bc8b305964e38af47f28f6914812300f6d41f0c0566217d296`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 6.4 MB (6427791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86a1d8eebb14b18f95482b5fed7f7db921edb4a36923a1fa729a8ff9a51e60c`  
		Last Modified: Tue, 30 Sep 2025 20:26:06 GMT  
		Size: 237.6 MB (237589431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023959bd9272a6e302a2b0fb8896601ccdcd968a4a0a55cc328b342907b505a8`  
		Last Modified: Mon, 29 Sep 2025 23:56:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:7296725d9ab598015ca98612df843236f5ad8e5927904e8e39149ecee557367a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ceb7ad92ad886a174b1c6d5f3ac1377b18e259d1d546188e0357f79a0b462f`

```dockerfile
```

-	Layers:
	-	`sha256:b9b6e117d660f20a6c91c880c4e66c91af9b349e29b30e3c9bff4e182715fd91`  
		Last Modified: Tue, 30 Sep 2025 02:02:33 GMT  
		Size: 2.2 MB (2237164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:438071e2dc49ef212a56700c5088515884d11d48893d846ff0f95eb1129395d6`  
		Last Modified: Tue, 30 Sep 2025 02:02:34 GMT  
		Size: 18.3 KB (18318 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:5912f029cf4d6321609eb33edd16b4575a95e02133ad8f265aea647bc6106758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f94b0200351f6e3cbc79f6dfa221b3a8e7ed38e4eaecb69e1e2c1100f7c348`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 16 Sep 2025 05:59:21 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eacc49f7bf2458ec893d7ca865565eb537730cc1a8c8192c5b92db80296ece6`  
		Last Modified: Tue, 30 Sep 2025 06:57:23 GMT  
		Size: 6.7 MB (6682252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aff53bcbf0ccfa4a12e4dba0e15bb49d8680f56beb5cc7ccd42cd6457b378a8`  
		Last Modified: Wed, 01 Oct 2025 20:33:37 GMT  
		Size: 248.6 MB (248575957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4b71d712ca77414bef94e96e73dc8dc72bf2a2b989066359f0d2906731839`  
		Last Modified: Tue, 30 Sep 2025 06:57:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:47fec0456536af0001ea180916b0432a4bc6ac82253a6ddbe3fec286bebe8ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2262234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e044ef29fabba4707cff9eac02801052116c43482dcfe92b47e18a4f00195ed`

```dockerfile
```

-	Layers:
	-	`sha256:5c88bb84b3dc2a651eabf5bb5fbfc4c918360e8227659dd36a5382a8c6bdcf9c`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 2.2 MB (2243792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183a871be75345d47a3f5a3fa6b872549f7110591f2e64b1aed193fc9a8505d8`  
		Last Modified: Wed, 01 Oct 2025 20:02:27 GMT  
		Size: 18.4 KB (18442 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-windowsservercore`

```console
$ docker pull julia@sha256:8a3401a95c02b86a61976194f946720c8a71e4ac3f104b78089d02b3004f3d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.11.7-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:ac38828597ed9bc945af1f4c4d588f85f3dd9846b6f8cb011a1a0cbd741a71c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3857533541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e33deb4d788a9bc8e0ff97d7533b9acb9fe5080668181f9c72c773d96fb2fb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 16 Sep 2025 17:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:35:33 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:35:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:35:35 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:37:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:37:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742bac5f17e737de033ac777c204f1da3eaed901a8ab4824de82bddcb635f97`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76f7fb7bd665fc8faa00d7204a8760a0db2c5299d75e53d32beb09a7095c13a`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081524dee08f1cf8f958c8175ede4627342d6e474edfaaef65e5a7d3090a0ad`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197bcfee6f005fecea1c486189f5d490e414368b3f87c57e104e54c1f55f2e8d`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50561f1b5d3a6703b4542e900ae8cd5e04398a6ea9797d662272ab7ed952d1`  
		Last Modified: Tue, 16 Sep 2025 20:03:22 GMT  
		Size: 286.1 MB (286087265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96a781c701973f728528c3ed6085d8cd7747d1bcb783559181b3bda9e6878`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:4ecd2ef8c4f890f85b0c8c26e46bc9d6888e96f921034b131e8addd69443ab3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568142462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8ca6e16146fedaef00cd44d27ace88bb27eb06350fe87df9be881480133657`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 16 Sep 2025 17:26:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:26:50 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:28:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da14a5aec402a0258fb230e5287bd5c53cb7fb91a9da0beac007e12b1521a9e`  
		Last Modified: Tue, 16 Sep 2025 17:28:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0d4d7fec49929952b1b90327e5f276863c5a95c0fe43f75843eb46e0953683`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc98f37b821fa6fa2d39022f2edd7ee706fb98375d308b9f6a9c8c9656e9e`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc28737c5b2f8a60d5b2ad12cff93a80cb1e8b281a83903d33fb781c18802`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b745b8cf856d2e683248255707cd8effb563b362c6b8bf774427905284459906`  
		Last Modified: Tue, 16 Sep 2025 20:03:45 GMT  
		Size: 286.0 MB (285990940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815888fad5b56125ed2f55bc222bf9674af3c17ecc01a775aaed551d174baae2`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:a0e25784c6fc13b850e0a7f6f69372ad1a91862652141185ff5ca4a538ba5910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1.11.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:4ecd2ef8c4f890f85b0c8c26e46bc9d6888e96f921034b131e8addd69443ab3a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568142462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8ca6e16146fedaef00cd44d27ace88bb27eb06350fe87df9be881480133657`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Tue, 16 Sep 2025 17:26:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:26:49 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:26:50 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:28:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da14a5aec402a0258fb230e5287bd5c53cb7fb91a9da0beac007e12b1521a9e`  
		Last Modified: Tue, 16 Sep 2025 17:28:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0d4d7fec49929952b1b90327e5f276863c5a95c0fe43f75843eb46e0953683`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64dc98f37b821fa6fa2d39022f2edd7ee706fb98375d308b9f6a9c8c9656e9e`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648fc28737c5b2f8a60d5b2ad12cff93a80cb1e8b281a83903d33fb781c18802`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b745b8cf856d2e683248255707cd8effb563b362c6b8bf774427905284459906`  
		Last Modified: Tue, 16 Sep 2025 20:03:45 GMT  
		Size: 286.0 MB (285990940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815888fad5b56125ed2f55bc222bf9674af3c17ecc01a775aaed551d174baae2`  
		Last Modified: Tue, 16 Sep 2025 17:29:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fc177cf1115dd82b4737d48635b23655e9ccae982714ccaff769924ba6b962bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1.11.7-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:ac38828597ed9bc945af1f4c4d588f85f3dd9846b6f8cb011a1a0cbd741a71c9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3857533541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e33deb4d788a9bc8e0ff97d7533b9acb9fe5080668181f9c72c773d96fb2fb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 16 Sep 2025 17:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Sep 2025 17:35:33 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 16 Sep 2025 17:35:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 16 Sep 2025 17:35:35 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 16 Sep 2025 17:37:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 16 Sep 2025 17:37:56 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4742bac5f17e737de033ac777c204f1da3eaed901a8ab4824de82bddcb635f97`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76f7fb7bd665fc8faa00d7204a8760a0db2c5299d75e53d32beb09a7095c13a`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8081524dee08f1cf8f958c8175ede4627342d6e474edfaaef65e5a7d3090a0ad`  
		Last Modified: Tue, 16 Sep 2025 17:54:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197bcfee6f005fecea1c486189f5d490e414368b3f87c57e104e54c1f55f2e8d`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab50561f1b5d3a6703b4542e900ae8cd5e04398a6ea9797d662272ab7ed952d1`  
		Last Modified: Tue, 16 Sep 2025 20:03:22 GMT  
		Size: 286.1 MB (286087265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e96a781c701973f728528c3ed6085d8cd7747d1bcb783559181b3bda9e6878`  
		Last Modified: Tue, 16 Sep 2025 17:54:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12`

```console
$ docker pull julia@sha256:d5d792f8fedb069a90527a3d632ce4510a90c32411d8a72fdf0d1935ee6df9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.12` - linux; amd64

```console
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-bookworm`

```console
$ docker pull julia@sha256:99ddf36d97eaa12ca9e43d81d9d70025aa280ecd3d45b0e1f94d291d2bbe3782
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
$ docker pull julia@sha256:70230d2c81d4ab3554a0334bda465610d9cce461111fa141d144a2148114c22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319506830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903d66d0bffa44a76611abe66dea2fe89cd25b87fe95e848fd8de7a9c3a867f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca811ac4307c1488b6cbd2dc62d7c1c078ca5a4cacf34e3ffc9b29c7b4ef751c`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 5.7 MB (5716323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b508acb0220a8b7f26c2acc53b6c3a0fd53c4a00d2f877eac41e1e3fcd90d`  
		Last Modified: Wed, 08 Oct 2025 20:16:45 GMT  
		Size: 285.6 MB (285561802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f204c56b62295f834ff92a332d566df85fd81d75c9a4fde2c77580e6adde2d18`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a4b333091e24508599a8b4a6030f4ad8262038f98c1df050e1d3c100674bd76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668e975d30b0146d868bbcca6f61460b2089b6663dff4d82904e438215e4d962`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9ea196137e278ca2a0f42bb7af728b85cdabd4935748d40835e893ef0bf6a`  
		Last Modified: Wed, 08 Oct 2025 23:02:39 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a306454b16d0438c2a002d23e1c75044bb30b3b373e0dbed643c477681e686`  
		Last Modified: Wed, 08 Oct 2025 23:02:40 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d7d84080e9e6b24a1769bf0a011b69cfb724c6dbf0108c5aad4cadeab63fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339278659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a275f979d0c3cbaaf31b3da876e643e4ab62a1ac8ece3ae4df2392d0961efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f4ce1b9a56f84c283da7334e6218a33edfd2259168bc23fd77e9ea9b3f268`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 5.6 MB (5567102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2848785684a344ab32295e4c355472ff20a0be6c4b7f566098935a7361de73`  
		Last Modified: Wed, 08 Oct 2025 20:16:54 GMT  
		Size: 305.6 MB (305609040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11b9d3dca8c47b9cfcf2e28410520354f664aba6d18d1444c83a385940bd15e`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f1e1e094704c4b93414f41628e6a955518a9aeb7dbe51cfc74199d372e088637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66118456964de660d6987e1ebbe49fb01de41efa91d6f3d755086418d8ce952`

```dockerfile
```

-	Layers:
	-	`sha256:84eb79e0de87050b0a5e9c40fffbeda7996d073878db251c2e746a40a64e227a`  
		Last Modified: Wed, 08 Oct 2025 23:02:44 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6e711a3ba83235e573cf41124ee406a2abd99d3a3970225c8aec65286d0f09`  
		Last Modified: Wed, 08 Oct 2025 23:02:45 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f23beae460e2708631a53cb8cd2af35961c5d5f349c84c721e2a8086900de98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264787439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c0bb3b86a0374fd06c8ee1c1fb4719f8a2a1c4c8c2361141aa8bce9cd0669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c0f47338b353fb5108e63ba21f537e410d3adc552ada9dc6c79cc939a752d`  
		Last Modified: Wed, 08 Oct 2025 20:18:25 GMT  
		Size: 5.9 MB (5878120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077e9399fc8d6edf70bca86e878d6c21d631ab38ea31043f266040cb086afdf5`  
		Last Modified: Wed, 08 Oct 2025 20:17:57 GMT  
		Size: 229.7 MB (229699316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52568e110dd581bd9967bf126633450eac3ccab20598c6ae9a1d6f68fe9e326`  
		Last Modified: Wed, 08 Oct 2025 20:18:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1872746b5da92b8f9dfd97fef1370b4e1005521741d180cacd0c89f3bf8cb0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699abf8319ba3b4cf8234888f9a258fa360d4dc15eb0986f2097d1a39bf2758e`

```dockerfile
```

-	Layers:
	-	`sha256:3a00f81b981ec175e6d7695807b6b5bb2bc871645ec3694439d9cfa733479c2b`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f04ed6bb80e87a156b6f93281ea06fb604b3fe93b5ec49d27a31d503d5acff`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-trixie`

```console
$ docker pull julia@sha256:5b0938cb249a46258dc3c0dfa4541829ef2811dfbcf0b0c4272feccce7074dd0
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
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-windowsservercore`

```console
$ docker pull julia@sha256:743d12f48c5e16cb9bfc0a8ea9fa3a500d8dc65a90e424a38994874724126c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.12-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:86957bc28b8cbc3c9df766b39ba1f643f57055b89c1e34c9f87f1c110ba899ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:a4720044b1d9b33354bdba6060ce8864927053db2fa365144a263cb7eb3a4c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1.12-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.0`

```console
$ docker pull julia@sha256:d5d792f8fedb069a90527a3d632ce4510a90c32411d8a72fdf0d1935ee6df9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.12.0` - linux; amd64

```console
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.0` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.0-bookworm`

```console
$ docker pull julia@sha256:99ddf36d97eaa12ca9e43d81d9d70025aa280ecd3d45b0e1f94d291d2bbe3782
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.0-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:70230d2c81d4ab3554a0334bda465610d9cce461111fa141d144a2148114c22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319506830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903d66d0bffa44a76611abe66dea2fe89cd25b87fe95e848fd8de7a9c3a867f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca811ac4307c1488b6cbd2dc62d7c1c078ca5a4cacf34e3ffc9b29c7b4ef751c`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 5.7 MB (5716323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b508acb0220a8b7f26c2acc53b6c3a0fd53c4a00d2f877eac41e1e3fcd90d`  
		Last Modified: Wed, 08 Oct 2025 20:16:45 GMT  
		Size: 285.6 MB (285561802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f204c56b62295f834ff92a332d566df85fd81d75c9a4fde2c77580e6adde2d18`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a4b333091e24508599a8b4a6030f4ad8262038f98c1df050e1d3c100674bd76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668e975d30b0146d868bbcca6f61460b2089b6663dff4d82904e438215e4d962`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9ea196137e278ca2a0f42bb7af728b85cdabd4935748d40835e893ef0bf6a`  
		Last Modified: Wed, 08 Oct 2025 23:02:39 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a306454b16d0438c2a002d23e1c75044bb30b3b373e0dbed643c477681e686`  
		Last Modified: Wed, 08 Oct 2025 23:02:40 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d7d84080e9e6b24a1769bf0a011b69cfb724c6dbf0108c5aad4cadeab63fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339278659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a275f979d0c3cbaaf31b3da876e643e4ab62a1ac8ece3ae4df2392d0961efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f4ce1b9a56f84c283da7334e6218a33edfd2259168bc23fd77e9ea9b3f268`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 5.6 MB (5567102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2848785684a344ab32295e4c355472ff20a0be6c4b7f566098935a7361de73`  
		Last Modified: Wed, 08 Oct 2025 20:16:54 GMT  
		Size: 305.6 MB (305609040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11b9d3dca8c47b9cfcf2e28410520354f664aba6d18d1444c83a385940bd15e`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f1e1e094704c4b93414f41628e6a955518a9aeb7dbe51cfc74199d372e088637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66118456964de660d6987e1ebbe49fb01de41efa91d6f3d755086418d8ce952`

```dockerfile
```

-	Layers:
	-	`sha256:84eb79e0de87050b0a5e9c40fffbeda7996d073878db251c2e746a40a64e227a`  
		Last Modified: Wed, 08 Oct 2025 23:02:44 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6e711a3ba83235e573cf41124ee406a2abd99d3a3970225c8aec65286d0f09`  
		Last Modified: Wed, 08 Oct 2025 23:02:45 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0-bookworm` - linux; 386

```console
$ docker pull julia@sha256:f23beae460e2708631a53cb8cd2af35961c5d5f349c84c721e2a8086900de98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264787439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c0bb3b86a0374fd06c8ee1c1fb4719f8a2a1c4c8c2361141aa8bce9cd0669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c0f47338b353fb5108e63ba21f537e410d3adc552ada9dc6c79cc939a752d`  
		Last Modified: Wed, 08 Oct 2025 20:18:25 GMT  
		Size: 5.9 MB (5878120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077e9399fc8d6edf70bca86e878d6c21d631ab38ea31043f266040cb086afdf5`  
		Last Modified: Wed, 08 Oct 2025 20:17:57 GMT  
		Size: 229.7 MB (229699316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52568e110dd581bd9967bf126633450eac3ccab20598c6ae9a1d6f68fe9e326`  
		Last Modified: Wed, 08 Oct 2025 20:18:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1872746b5da92b8f9dfd97fef1370b4e1005521741d180cacd0c89f3bf8cb0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699abf8319ba3b4cf8234888f9a258fa360d4dc15eb0986f2097d1a39bf2758e`

```dockerfile
```

-	Layers:
	-	`sha256:3a00f81b981ec175e6d7695807b6b5bb2bc871645ec3694439d9cfa733479c2b`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f04ed6bb80e87a156b6f93281ea06fb604b3fe93b5ec49d27a31d503d5acff`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.0-trixie`

```console
$ docker pull julia@sha256:5b0938cb249a46258dc3c0dfa4541829ef2811dfbcf0b0c4272feccce7074dd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.0-trixie` - linux; amd64

```console
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.0-trixie` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.0-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.0-windowsservercore`

```console
$ docker pull julia@sha256:743d12f48c5e16cb9bfc0a8ea9fa3a500d8dc65a90e424a38994874724126c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:1.12.0-windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.0-windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.0-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:86957bc28b8cbc3c9df766b39ba1f643f57055b89c1e34c9f87f1c110ba899ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:1.12.0-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.0-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:a4720044b1d9b33354bdba6060ce8864927053db2fa365144a263cb7eb3a4c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:1.12.0-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:99ddf36d97eaa12ca9e43d81d9d70025aa280ecd3d45b0e1f94d291d2bbe3782
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
$ docker pull julia@sha256:70230d2c81d4ab3554a0334bda465610d9cce461111fa141d144a2148114c22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319506830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903d66d0bffa44a76611abe66dea2fe89cd25b87fe95e848fd8de7a9c3a867f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca811ac4307c1488b6cbd2dc62d7c1c078ca5a4cacf34e3ffc9b29c7b4ef751c`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 5.7 MB (5716323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69b508acb0220a8b7f26c2acc53b6c3a0fd53c4a00d2f877eac41e1e3fcd90d`  
		Last Modified: Wed, 08 Oct 2025 20:16:45 GMT  
		Size: 285.6 MB (285561802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f204c56b62295f834ff92a332d566df85fd81d75c9a4fde2c77580e6adde2d18`  
		Last Modified: Wed, 08 Oct 2025 20:17:13 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a4b333091e24508599a8b4a6030f4ad8262038f98c1df050e1d3c100674bd76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668e975d30b0146d868bbcca6f61460b2089b6663dff4d82904e438215e4d962`

```dockerfile
```

-	Layers:
	-	`sha256:d5a9ea196137e278ca2a0f42bb7af728b85cdabd4935748d40835e893ef0bf6a`  
		Last Modified: Wed, 08 Oct 2025 23:02:39 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a306454b16d0438c2a002d23e1c75044bb30b3b373e0dbed643c477681e686`  
		Last Modified: Wed, 08 Oct 2025 23:02:40 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4d7d84080e9e6b24a1769bf0a011b69cfb724c6dbf0108c5aad4cadeab63fb4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.3 MB (339278659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a275f979d0c3cbaaf31b3da876e643e4ab62a1ac8ece3ae4df2392d0961efa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f4ce1b9a56f84c283da7334e6218a33edfd2259168bc23fd77e9ea9b3f268`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 5.6 MB (5567102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2848785684a344ab32295e4c355472ff20a0be6c4b7f566098935a7361de73`  
		Last Modified: Wed, 08 Oct 2025 20:16:54 GMT  
		Size: 305.6 MB (305609040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11b9d3dca8c47b9cfcf2e28410520354f664aba6d18d1444c83a385940bd15e`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f1e1e094704c4b93414f41628e6a955518a9aeb7dbe51cfc74199d372e088637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66118456964de660d6987e1ebbe49fb01de41efa91d6f3d755086418d8ce952`

```dockerfile
```

-	Layers:
	-	`sha256:84eb79e0de87050b0a5e9c40fffbeda7996d073878db251c2e746a40a64e227a`  
		Last Modified: Wed, 08 Oct 2025 23:02:44 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6e711a3ba83235e573cf41124ee406a2abd99d3a3970225c8aec65286d0f09`  
		Last Modified: Wed, 08 Oct 2025 23:02:45 GMT  
		Size: 16.7 KB (16703 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:f23beae460e2708631a53cb8cd2af35961c5d5f349c84c721e2a8086900de98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264787439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4c0bb3b86a0374fd06c8ee1c1fb4719f8a2a1c4c8c2361141aa8bce9cd0669`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94c0f47338b353fb5108e63ba21f537e410d3adc552ada9dc6c79cc939a752d`  
		Last Modified: Wed, 08 Oct 2025 20:18:25 GMT  
		Size: 5.9 MB (5878120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077e9399fc8d6edf70bca86e878d6c21d631ab38ea31043f266040cb086afdf5`  
		Last Modified: Wed, 08 Oct 2025 20:17:57 GMT  
		Size: 229.7 MB (229699316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52568e110dd581bd9967bf126633450eac3ccab20598c6ae9a1d6f68fe9e326`  
		Last Modified: Wed, 08 Oct 2025 20:18:24 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1872746b5da92b8f9dfd97fef1370b4e1005521741d180cacd0c89f3bf8cb0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699abf8319ba3b4cf8234888f9a258fa360d4dc15eb0986f2097d1a39bf2758e`

```dockerfile
```

-	Layers:
	-	`sha256:3a00f81b981ec175e6d7695807b6b5bb2bc871645ec3694439d9cfa733479c2b`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8f04ed6bb80e87a156b6f93281ea06fb604b3fe93b5ec49d27a31d503d5acff`  
		Last Modified: Wed, 08 Oct 2025 23:02:49 GMT  
		Size: 16.6 KB (16550 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:d5d792f8fedb069a90527a3d632ce4510a90c32411d8a72fdf0d1935ee6df9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:trixie`

```console
$ docker pull julia@sha256:5b0938cb249a46258dc3c0dfa4541829ef2811dfbcf0b0c4272feccce7074dd0
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
$ docker pull julia@sha256:b1d137e42630a0f11a15fcfeb3eff34592de092ac91886d61a2e79a72634c573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324562819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0086026d44681bbda886924136a74108d4f417df4acc87739d64e52ee19a65a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54be80471da9ff8e585edb560ed301e2075f8befd524c9a73aba57cf727726e7`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 9.2 MB (9199640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e74da6e49c1e21992888660b8cd00b656ce0510b6a8d763e5d688c76acd1cc7`  
		Last Modified: Wed, 08 Oct 2025 20:24:41 GMT  
		Size: 285.6 MB (285585042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b54d1b7ba9797581f0aca65608179cc156d2551303f36430f2d592af1eb28b`  
		Last Modified: Wed, 08 Oct 2025 20:17:04 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dc5538a0e3934380b87c96320f9b6423f4e958e95a41bacced453e096aca08c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03fceef92316a174ec63a76625a8331a127d90b9b7692273bf17a8904c0553fe`

```dockerfile
```

-	Layers:
	-	`sha256:be7781b899261218869d02e3ac2bf93ca83d5a70fac457354b38a0ba77ab7f20`  
		Last Modified: Wed, 08 Oct 2025 23:02:28 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05fd93fec77df7cb301bb50525c95ca848b8f70afc9984ffd743b63d7db3a33d`  
		Last Modified: Wed, 08 Oct 2025 23:02:29 GMT  
		Size: 17.7 KB (17726 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:36f06979aded3c9fdd37794f3f50b62bb7c4490fec936aa82b87bc5f0775bf7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345264985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4ade9eecd45ba11ebec62d7348dfb3d5fed616281c38845a56155324d98588`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0692ff09c7fa722aefb06c7dab5c5457bce9a0c6da38ac068f0ca8915797097`  
		Last Modified: Wed, 08 Oct 2025 20:17:10 GMT  
		Size: 9.5 MB (9471250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbb9e7799e6868887bc438c4159fceb727ed990b1a166417849777382eb43c8`  
		Last Modified: Wed, 08 Oct 2025 20:25:07 GMT  
		Size: 305.7 MB (305652520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8ec5192fd9f63b748dba746c0763549b2071eb43b6d1f799af039d3b6f6aec`  
		Last Modified: Wed, 08 Oct 2025 20:17:07 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:54cec3b8701a132c5f01365e7c6cd3be6fa45f6b155e0cc460071cb91f253a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd685366ed45c4d5f1addee85a4aebb8de28c7189aaa9df1b108c0be00c001b`

```dockerfile
```

-	Layers:
	-	`sha256:84e8d94a3fa0d121dca2b87a5e2eff5566ddff74520a297aedf379d7854b2e08`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7198ba04f4cd513591c9706972a2dd44b7245518fd9f793f398135fd8e5eee1`  
		Last Modified: Wed, 08 Oct 2025 23:02:33 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:8375c931c9c82619a0fea5f00acb4b64743abe1ea6b5188f2eab959fc8113ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.3 MB (270334553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d29afb39e3c9e7c45a62523c92d735c64fde73d24ac2f16eee92ceaca78787`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 08 Oct 2025 05:59:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 08 Oct 2025 05:59:24 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 05:59:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-linux-x86_64.tar.gz'; 			sha256='6f87b8fcf5ef6a7371e8c79d948aedfa0ba28ce44447c446d7d82e70f0158da8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-linux-aarch64.tar.gz'; 			sha256='0fb44de10c3a9da719b4962c2158fe4484d98377e521318b692e91a1bea5716b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-linux-i686.tar.gz'; 			sha256='bef313ad70b3b3131a879118a388a878cb6e0aceab018f8dbf01de247d31f705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 08 Oct 2025 05:59:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Oct 2025 05:59:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd442d879403047760fa0d6f64f2bff8ed107adca7e7a33dfe3870d54e81fc9`  
		Last Modified: Wed, 08 Oct 2025 20:18:09 GMT  
		Size: 9.3 MB (9311897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392f4849bb3dd8b081e1718368fc337133a5e2ff32e0c1be58251fa7cad67bd`  
		Last Modified: Wed, 08 Oct 2025 20:26:10 GMT  
		Size: 229.7 MB (229727750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e7e9ff6fb680d158358e563aa60978e8c51ae34d4760b30e9427be5f6f7716`  
		Last Modified: Wed, 08 Oct 2025 20:18:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:76ff4517f85fbaec457353c76f1f3a6e7127b77ae8f33fd1ce7e4635677bc53b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f64751e6e850f1d8ba8b1e128f7febec9ec7adbc0e64a63231260352386b8`

```dockerfile
```

-	Layers:
	-	`sha256:2b765972bb92ec6d9fcfd3575fd47777b8ae119b0da6c074827ada98dd844cb5`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1940e785ba9274a7ad78165007cd03a60ed099f4e1c5c22595101485baaca188`  
		Last Modified: Wed, 08 Oct 2025 23:02:38 GMT  
		Size: 17.7 KB (17672 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:743d12f48c5e16cb9bfc0a8ea9fa3a500d8dc65a90e424a38994874724126c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:windowsservercore` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:86957bc28b8cbc3c9df766b39ba1f643f57055b89c1e34c9f87f1c110ba899ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:b666e4aaf463689b2659516980e32efd979d41b2a2d7b737e6fd438fe17c01be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579684863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b5c757ace3879e7e747ff537c447d31811d740c3f85a06150def2340bb6c4e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 08 Oct 2025 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:25:53 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:25:54 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:28:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b724ac801cd8cb9ba53dd10acd40a2578e08d4384ebd856252a639e5c6a7de23`  
		Last Modified: Wed, 08 Oct 2025 20:26:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6396ccd403ed67ac2efa272f7bdc1fefa8e7842d7070c2e939a209ded3463a6e`  
		Last Modified: Wed, 08 Oct 2025 20:39:30 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31429b56e7a37e48ec1eaf094a6d791969a482c7491962be14504b89e4708722`  
		Last Modified: Wed, 08 Oct 2025 20:39:35 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c60515e5bd172d41d3051e9cf33c962678483d67ea22edcece386627ba97d89`  
		Last Modified: Wed, 08 Oct 2025 20:39:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb0b1498790da068713e1f33cee858133da91b490f8a6469dea0f2a91b30143`  
		Last Modified: Wed, 08 Oct 2025 23:03:40 GMT  
		Size: 297.5 MB (297533355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee36bb82c47788b53f4d8cf22938d708dcf9378fc2c80b2f0e42b19a2c98665`  
		Last Modified: Wed, 08 Oct 2025 20:39:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:a4720044b1d9b33354bdba6060ce8864927053db2fa365144a263cb7eb3a4c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:27a6dece62e71d03b75914cff736dd73cf3ad8b8887148c72610ac84d76af931
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869027886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea4bb0d15506e3c0d4a2e216c1e667059155d4a8b0794b465912ba0ac712551b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 08 Oct 2025 20:24:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_VERSION=1.12.0
# Wed, 08 Oct 2025 20:24:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-win64.exe
# Wed, 08 Oct 2025 20:24:06 GMT
ENV JULIA_SHA256=1dd9ea0e4b61dfe5bc4d81e37e4cf19acb4f65b09699e3a4c65ba6ac727d7a3f
# Wed, 08 Oct 2025 20:25:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 08 Oct 2025 20:25:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fff894853341ead75bb5f471045245bccd651807e46b69a7bd539a2919e3b`  
		Last Modified: Wed, 08 Oct 2025 20:26:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf02188c8044e5da02958f7cd2f53b63dc85b72504cf89b625c83f94359991`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81926720790c71d5cde92ed16a4d0d9161d911fabc314ca758007ab0444e6be5`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13280ae4ddbdb0f9611a5a4f7b7741002145f5c277aa6c26d521d65791ebaf61`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21898f4a63ab5a2a08b1cb43d7ea0c4375d7868a30486c33eaf507e9d1bda11`  
		Last Modified: Wed, 08 Oct 2025 23:02:59 GMT  
		Size: 297.6 MB (297581585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706c112903d759bccf25ad1e7ad93657f4a80db4e5dd75a7cf7fdc219ed6b578`  
		Last Modified: Wed, 08 Oct 2025 20:26:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
