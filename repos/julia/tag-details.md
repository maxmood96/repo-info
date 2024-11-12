<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.19`](#julia110-alpine319)
-	[`julia:1.10-alpine3.20`](#julia110-alpine320)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-bullseye`](#julia110-bullseye)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-1809`](#julia110-windowsservercore-1809)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10.6`](#julia1106)
-	[`julia:1.10.6-alpine`](#julia1106-alpine)
-	[`julia:1.10.6-alpine3.19`](#julia1106-alpine319)
-	[`julia:1.10.6-alpine3.20`](#julia1106-alpine320)
-	[`julia:1.10.6-bookworm`](#julia1106-bookworm)
-	[`julia:1.10.6-bullseye`](#julia1106-bullseye)
-	[`julia:1.10.6-windowsservercore`](#julia1106-windowsservercore)
-	[`julia:1.10.6-windowsservercore-1809`](#julia1106-windowsservercore-1809)
-	[`julia:1.10.6-windowsservercore-ltsc2022`](#julia1106-windowsservercore-ltsc2022)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-bullseye`](#julia111-bullseye)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-1809`](#julia111-windowsservercore-1809)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11.1`](#julia1111)
-	[`julia:1.11.1-bookworm`](#julia1111-bookworm)
-	[`julia:1.11.1-bullseye`](#julia1111-bullseye)
-	[`julia:1.11.1-windowsservercore`](#julia1111-windowsservercore)
-	[`julia:1.11.1-windowsservercore-1809`](#julia1111-windowsservercore-1809)
-	[`julia:1.11.1-windowsservercore-ltsc2022`](#julia1111-windowsservercore-ltsc2022)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:5cf1f32cf1d3836ff87a0614efb58e7c7ec84ca3fa6785efc317e19154cfded0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:46803c478e2350ee2ec92eb18c58b172064acc26b43ddbd6739173173758bf99
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
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:ec93afc7220f9a01c0b7f50a5fff3e7fcfe8edbbcac52c005cf79267185dcd1b
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
$ docker pull julia@sha256:6ad1f47f6bb14abd9094fbe7ac2f7e8713922b08f8bc167b527b2403ac32c3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290772899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cf8d3dc0fc2427f42f0cf27f89a7328b49f7cc84ae385e42505875d60b118`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90e228fdb2b7decf92841af0c19add44ea11f38fcccc06b67e0c351d0c0f53`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.2 MB (2222723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5ad4ee1a7abf803e6947c14b525b93e982ced55a5c28f8e01d8d0d91274c2f`  
		Last Modified: Tue, 12 Nov 2024 02:03:46 GMT  
		Size: 257.1 MB (257098246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4bd9a096e04ad4efce79ea96e89ab73d28e939ea033cdf4cdeb09371c39b8a`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e84cbbdf7a63dcee3e8f8a6eb5f72fc71e8c852aa4bee18c2470630e521e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9102b91fab566df758f1323e7f62fd57b103df327c4c2691548fe70edd2b8a13`

```dockerfile
```

-	Layers:
	-	`sha256:8b29c2f1c5db4ecd50d839c3a0fbac2f2a2939dcd6a57dd3bd99143eab64afa5`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.7 MB (2717035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57de41a80224d8c0897e41e665d25ee9ad4ae7344f650f87a23a3f3cb5fdd2c8`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6f833498ed7451c126fc9114e09c938071fcdc172068faa9c07621b498bf1e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286308812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c83668c2dc30778d6eb47e259cd5798cbd50fef427f433f63feccb51126666`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d503ab39ed3cdd3f8d0a29b0b3ee1941169aba3493d0ccb5ea9ff12821b3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.2 MB (2210272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb865f98aa3d1aa03080b347b6b4951da76e34c127c12b3ad122ee6ae788de66`  
		Last Modified: Tue, 12 Nov 2024 03:17:28 GMT  
		Size: 254.0 MB (254006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192e63792f6ee32a588d7580f44fd2dd8213eb64be51dfa38e4d06e2c08b45b`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cc59ebca35370f7217603a1df7120b5f5712900f31318bcba7c1289fbed5f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318ae46fdd8c646ad00da5ba9754f2f9209887473826a38e000cf260ca282e8`

```dockerfile
```

-	Layers:
	-	`sha256:5a79359a4ca09a47591c34ca139874ad937e3ef4fcfe00f8b027fc309d959563`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.7 MB (2717297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031b66b179eb4d2ca81bcc90cf94668aeff3314707742239d0036d0fea1018e3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2928e66b6e739ba1a7677026582e0dcb011a56b214b521ada383940e5c9e1853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269410481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4477a6226df30b1aee6fbf7bf27dd29b1a5d6ed67f0861f3daaa9de2239a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d452f6a4c4aebe891a7d111deaa15df8668219b2dcf00736127fee1208a5e0d`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.3 MB (2328167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daaec2aac82defed7f37a975c8ed6547bf042c092d9660c50d3b9e07cdf58e0`  
		Last Modified: Tue, 12 Nov 2024 02:03:34 GMT  
		Size: 234.7 MB (234658597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7226831f566cb96842ea556ee18df519c2b14c3a30976f87f6eeb967085b6`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2aa198ddc7916c5b5315ef43ffccc612a5cc2a49b8743c02ded0b47eeeffb17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1de9bbadaed9fdfd49e994f78e3429dcc4cce152e0b8031fda2c978eb074eef`

```dockerfile
```

-	Layers:
	-	`sha256:3851f1a748150fe57188c5c8c5cfe69d2756c1b7e0433e5942d029ae64c69f77`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.7 MB (2714133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10734275766cf0df9be09554590c38267f13e935a48a61525fe313c7fb353429`  
		Last Modified: Tue, 12 Nov 2024 02:03:28 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:304e5459ad48b82ee204697a59d8882698923d16314acbe0e9b4df90bff9a9fc
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:3aeafe8fef111e7073cb229623e822507822ab70ff032754f9bcd283a54fcc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211472178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba19a7a93cc178c1b065587a36e67da518fc48ff05e9300fc4d8a2027b18a9aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101adee98773e3e59fecdd887e2522c82747a6adcc91a254babc8ce166f83ada`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.7 MB (5713103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694fa0b0ac731e838a9379e1e4838cd0364ec17b215749e0494fd8364a01f18e`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 176.6 MB (176630711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b576fe205428e7457a4c4b9a480e81d65ccbff53d0d1aa12db2467b42b4d0`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:541a7abe5faf1739d10f182a28771ab86be8af1894a4319028284f9d4cf314e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20e8b60a2df1079f8a8fedaed593057da563b14c0bc4ac765f25c79d8ea0339`

```dockerfile
```

-	Layers:
	-	`sha256:2cb25d4138f2051c814b62f70099ef0fedeaf9c5f9b977d30f4d6d7ac8bd5ca3`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4be31bf4d664270127ffb78183e4abbbe8992903b096c010cf68e6473b6368`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:550f700ca18814aeb60a14bb3305385d3cebaf7b5db8a304fb4a2f8afdbca53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212043012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c31b68e3daba85eed82a663f11cdde057281b90fc7dc5576da4400849a5af3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94441d0ec70e24000d147d731879b8df09a90ade89414c00807401b585a4e344`  
		Last Modified: Tue, 12 Nov 2024 03:18:38 GMT  
		Size: 177.3 MB (177347250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dca3138d75dc5371de1d1506ac0e841b70132e76afd01bb4aa461c7dae441c`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:bd869a20569dbd9d256f228792d771507a079add37d7b8351546ba13aa98a6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34912f0906fc1e30b25afd6907d7fc970164e36b5362e726b27aa582d98ba18e`

```dockerfile
```

-	Layers:
	-	`sha256:52507a8bb01386617e76c7187069f4c817faf2c4f5eb45aa59ec1ee73e17844e`  
		Last Modified: Tue, 12 Nov 2024 03:18:34 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ecd40236b77b231ee24deb064bd5829a27583c167bb1943564c6913e4c7953`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:98c7a03e63cb4f4cc2581ea02fb1b1d015975e79db925da1cefcca3bbd74ab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193830763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916290621e529687cf43d50c0afcd5530885dc5d973278312158823e42fc4703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ccc2160ddf2d5a1ac2fd82f045731436b933d62a3567dc56ae446444246242`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 5.9 MB (5872110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae64e8c9c17e01b02c497d969bdd711fb52a21dc8dad450d92682337b67a7a`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 157.8 MB (157812833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b977eea4fa680c3b916e318a0d110cd539eb781779cfbb3792dba448d2778f`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:51c21a7faf1c686471eb59db5c1602aeaa52a33a6e23bc9fb675ad9708c26fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961459d1515bf19e1a9906c4e850c146bacf5b24b5190e09ec5d6f3aade67fcd`

```dockerfile
```

-	Layers:
	-	`sha256:ed8bc43d2238533bc2b97d27212c368e9a6e3745ee4733c4f17b536bd4d8f78c`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ca5c79fea5ce39612993be9346f6b7f5d5eb7f8c0b1058535c1ae7fed85a1`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:058d6048f5793495308f357bb305111bbd44713a6c92a9622df3e33fb32d0b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194682502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ec0f27255c38e1d25b100b57c80831baf5e7ae1e4cea3f7f254bd311c979fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5380f0969ba018b5e9f1ac8bc89d2c882dfc6f5713b4b32c3d01095483ad1f50`  
		Last Modified: Tue, 12 Nov 2024 02:56:00 GMT  
		Size: 155.3 MB (155307474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862ed6b3b616f194106cdb7ea8f1eb67b7600de9bb7d0dbb07e1928ce342945`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:aa36ec2e15282e201e9cab59e959865294c2620546e9a3caace21ade5d1857a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a851761cbac62b422c180a6540db2ed4146b483f62de584e6594226776586b5`

```dockerfile
```

-	Layers:
	-	`sha256:91f6db47e4d73faa28d3f003c755567b4ab5fce431b1e0b85d090ae464a6e991`  
		Last Modified: Tue, 12 Nov 2024 02:55:56 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ecdd39defabd1d11dfc2310ab08e80a419ffb0ed4406938cded9e7fcb4d765`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:f3973ab4ab6ef3b0f3f095a68a1e50dd2a0bf3884fa06b3cc60f49ba33cded14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:9812c83d818e41abd04df2b7cb5d963c24bbdb25bd098c02b5f0284f4a073277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b209bbb5f468c1fb71e00fbdeec0249a4fd34c0afea421a6327f37f9b81ed488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b151b060aa63746dd750e670ea5bdc1620a2092ab16549d04dcfa0a35be99a19`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 179.2 MB (179208171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b5fa518dc4207c412f265ae78a462120f7d1ca4429f61b221a864bd2ae4767`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:f1676098e123ba7b82a858b8f167109a730cd1eb3794682717776678add6ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 KB (86826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f0fa775c45dff7002ab8e42f1072159d5d435f423346b1b63f3ac42be509b`

```dockerfile
```

-	Layers:
	-	`sha256:0a7594e53064d03d5a486067821d62a0fe2806e32e1945dac733e9bec7712bb5`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e78df92e975c56c25b51babfa966c91cd333817b0d41a2ab67bd3ebcade3ead1`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.19`

```console
$ docker pull julia@sha256:03c9c31d6a720ea5ddf62e6f4179fa6c78b1443577b48ea6808f2c7e756d8b01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:accaafcfbbb155631e4a5174306213b4b5e414684bdebf6338565a73df9d866f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182628335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb22a575f4823a0b6af31c76a9ee92b9d07747b074ffcea98593d32b6fdae70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff76342ab75aef9ffda7369b4499fea8ac40f04447dcb223287661da9c8805ea`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 179.2 MB (179208239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cad05def77ae3f6ffa5a1536823eececb770333a073dbcc5616867b69582b3`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:412190df9c13b55eebe439aaa4359ac6589fa3aee0f29991f5ce7450137d5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 KB (89829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc08707821bbb23fe9bcbdd0357d465f40ae145d2f9930bb51672aa9c4a7d2a`

```dockerfile
```

-	Layers:
	-	`sha256:1cde15cb7c60ddac05cf3811e6a1f4326078328ce01b5cb2f2b04eaf452f01d9`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc582427fb65f80fe5a33c625e31ca63117ad4b103b38bcbdefaf8179ff8a8f`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.20`

```console
$ docker pull julia@sha256:f3973ab4ab6ef3b0f3f095a68a1e50dd2a0bf3884fa06b3cc60f49ba33cded14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:9812c83d818e41abd04df2b7cb5d963c24bbdb25bd098c02b5f0284f4a073277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b209bbb5f468c1fb71e00fbdeec0249a4fd34c0afea421a6327f37f9b81ed488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b151b060aa63746dd750e670ea5bdc1620a2092ab16549d04dcfa0a35be99a19`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 179.2 MB (179208171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b5fa518dc4207c412f265ae78a462120f7d1ca4429f61b221a864bd2ae4767`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:f1676098e123ba7b82a858b8f167109a730cd1eb3794682717776678add6ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 KB (86826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f0fa775c45dff7002ab8e42f1072159d5d435f423346b1b63f3ac42be509b`

```dockerfile
```

-	Layers:
	-	`sha256:0a7594e53064d03d5a486067821d62a0fe2806e32e1945dac733e9bec7712bb5`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e78df92e975c56c25b51babfa966c91cd333817b0d41a2ab67bd3ebcade3ead1`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:333b4a42171023dfc8fed32aec4d45504596f86686d5975710edcc29dc1b6555
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
$ docker pull julia@sha256:3aeafe8fef111e7073cb229623e822507822ab70ff032754f9bcd283a54fcc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211472178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba19a7a93cc178c1b065587a36e67da518fc48ff05e9300fc4d8a2027b18a9aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101adee98773e3e59fecdd887e2522c82747a6adcc91a254babc8ce166f83ada`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.7 MB (5713103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694fa0b0ac731e838a9379e1e4838cd0364ec17b215749e0494fd8364a01f18e`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 176.6 MB (176630711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b576fe205428e7457a4c4b9a480e81d65ccbff53d0d1aa12db2467b42b4d0`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:541a7abe5faf1739d10f182a28771ab86be8af1894a4319028284f9d4cf314e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20e8b60a2df1079f8a8fedaed593057da563b14c0bc4ac765f25c79d8ea0339`

```dockerfile
```

-	Layers:
	-	`sha256:2cb25d4138f2051c814b62f70099ef0fedeaf9c5f9b977d30f4d6d7ac8bd5ca3`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4be31bf4d664270127ffb78183e4abbbe8992903b096c010cf68e6473b6368`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:550f700ca18814aeb60a14bb3305385d3cebaf7b5db8a304fb4a2f8afdbca53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212043012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c31b68e3daba85eed82a663f11cdde057281b90fc7dc5576da4400849a5af3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94441d0ec70e24000d147d731879b8df09a90ade89414c00807401b585a4e344`  
		Last Modified: Tue, 12 Nov 2024 03:18:38 GMT  
		Size: 177.3 MB (177347250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dca3138d75dc5371de1d1506ac0e841b70132e76afd01bb4aa461c7dae441c`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bd869a20569dbd9d256f228792d771507a079add37d7b8351546ba13aa98a6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34912f0906fc1e30b25afd6907d7fc970164e36b5362e726b27aa582d98ba18e`

```dockerfile
```

-	Layers:
	-	`sha256:52507a8bb01386617e76c7187069f4c817faf2c4f5eb45aa59ec1ee73e17844e`  
		Last Modified: Tue, 12 Nov 2024 03:18:34 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ecd40236b77b231ee24deb064bd5829a27583c167bb1943564c6913e4c7953`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:98c7a03e63cb4f4cc2581ea02fb1b1d015975e79db925da1cefcca3bbd74ab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193830763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916290621e529687cf43d50c0afcd5530885dc5d973278312158823e42fc4703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ccc2160ddf2d5a1ac2fd82f045731436b933d62a3567dc56ae446444246242`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 5.9 MB (5872110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae64e8c9c17e01b02c497d969bdd711fb52a21dc8dad450d92682337b67a7a`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 157.8 MB (157812833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b977eea4fa680c3b916e318a0d110cd539eb781779cfbb3792dba448d2778f`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:51c21a7faf1c686471eb59db5c1602aeaa52a33a6e23bc9fb675ad9708c26fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961459d1515bf19e1a9906c4e850c146bacf5b24b5190e09ec5d6f3aade67fcd`

```dockerfile
```

-	Layers:
	-	`sha256:ed8bc43d2238533bc2b97d27212c368e9a6e3745ee4733c4f17b536bd4d8f78c`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ca5c79fea5ce39612993be9346f6b7f5d5eb7f8c0b1058535c1ae7fed85a1`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:058d6048f5793495308f357bb305111bbd44713a6c92a9622df3e33fb32d0b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194682502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ec0f27255c38e1d25b100b57c80831baf5e7ae1e4cea3f7f254bd311c979fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5380f0969ba018b5e9f1ac8bc89d2c882dfc6f5713b4b32c3d01095483ad1f50`  
		Last Modified: Tue, 12 Nov 2024 02:56:00 GMT  
		Size: 155.3 MB (155307474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862ed6b3b616f194106cdb7ea8f1eb67b7600de9bb7d0dbb07e1928ce342945`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:aa36ec2e15282e201e9cab59e959865294c2620546e9a3caace21ade5d1857a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a851761cbac62b422c180a6540db2ed4146b483f62de584e6594226776586b5`

```dockerfile
```

-	Layers:
	-	`sha256:91f6db47e4d73faa28d3f003c755567b4ab5fce431b1e0b85d090ae464a6e991`  
		Last Modified: Tue, 12 Nov 2024 02:55:56 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ecdd39defabd1d11dfc2310ab08e80a419ffb0ed4406938cded9e7fcb4d765`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bullseye`

```console
$ docker pull julia@sha256:87d036e9f4482746e413fc698cd0dc5d882a7919a25668256802a0cc230037a2
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
$ docker pull julia@sha256:9da1a5e74843f16f44629dd2e49761cbb851fefff24b0a6aa2b7039725db2617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210305686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f741341a68cfddfdeeb50bc6d743cdea87dbc97d03305e9616ab842dd9c198bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948cbffd20e08d7cd6e8bc9a1ac4ed59b132379617b89e0f98e1e06d8df494c9`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 2.2 MB (2222782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd109eef3e4613b36ea2b28d1f9e6c658d5f29939d7fbd68fe2484fe1dca42`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 176.6 MB (176630975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a826e971f361c507a3a036b2a2173a1b322902e9c82da4f3c8c301a1538b54`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:9f88dcf84d296911034b1ff03020ba556ce8b682d7d60c826b2659529db4f65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce9d2aa083e280cf947dab6cf89134ff957a48ca67656363fa6e472f8bb83bf`

```dockerfile
```

-	Layers:
	-	`sha256:768498f76dc4f302a83c727a37712a9e7ee842e5870fb8cf1646d17bbfced199`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 2.7 MB (2717653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54035c10a2e7fc4dafa6c5e78136f1cefedf66c89b6435957574c8794d2091f4`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e433c30dd4b33f9abcb1f281c4c3f39fe63149880256684d614d47c9e90c933b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209649976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20e6926fff5d295e4d315640ebcce594cd97602ce1a518e7df54a2c30ea852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d503ab39ed3cdd3f8d0a29b0b3ee1941169aba3493d0ccb5ea9ff12821b3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.2 MB (2210272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d2f4cb45ddcafd38f0bf2b839ff651a82cae793f523a9b9c94d92f92f0ac35`  
		Last Modified: Tue, 12 Nov 2024 03:19:41 GMT  
		Size: 177.3 MB (177347738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3241f2572494099db877cd9559471aa5083ebfbcd02fd7669bc87b0ae383ed`  
		Last Modified: Tue, 12 Nov 2024 03:19:36 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3390fae85a2ed3976607582c363d23a5f473c2efece8327c5d63b0402a527a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2733390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556b34c046c2408945e1713ca31a0f6ebdaf8d12c5b65f295415e7c2ae532f24`

```dockerfile
```

-	Layers:
	-	`sha256:2e0778fd08b654e9a4d6bba8ed048b8a6262f281260d7c06da239e310ede3bdf`  
		Last Modified: Tue, 12 Nov 2024 03:19:36 GMT  
		Size: 2.7 MB (2716669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458e274b5701a0ba44c9d646f415a1394f928aaf9f67d7f9c4ba14e998ff829f`  
		Last Modified: Tue, 12 Nov 2024 03:19:36 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2f5bf29934557f3fe5f20df7d3fda714f46ab7d00d1d78563da5ce2ea1347d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192565376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d760b242e12ae38909bbdf7ac1e4894db86b0f44efbad49f0d5730bafdd259d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed931e316242f942722ef7ebad630dd0cd42027c2f4415b19818833a3c2c9ec2`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.3 MB (2328131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add27b5406614d2e30c2e8ac830174651bc23c09cd51700a5131d706f269a7b7`  
		Last Modified: Tue, 12 Nov 2024 02:03:24 GMT  
		Size: 157.8 MB (157813525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa6432cf1844f28cfb2c33197977a66eeef33d48ca3c6994801c0abc58d3f0`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4f20694f7a6d3701cd66522fd54c45df571d0b55e1b3710431a4d667257d1d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13760d469cd1d8b7d0549cfa94236f381957c64830bf3048819a00d136f0aee`

```dockerfile
```

-	Layers:
	-	`sha256:9c92b2c816d747ff699a1984d3f7d27ffa25765dd8e1851f4755984e5edca047`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.7 MB (2714761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62291fccea8724347aca3fc10604cb54ac99007d5cb9f45042010064387a07a2`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:bad5fd470043108972fab03ab7fba19dd1a37e13481871a96cfaccc0c9a78304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-1809`

```console
$ docker pull julia@sha256:58087ae2d9648fa6b36d657e915e543117eeae1bb7dd7ecd19ab015510e67d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0e65c00e6c1db3fd045c6a7adc21172ef95b4163656cc090fe6155b59939459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6`

```console
$ docker pull julia@sha256:304e5459ad48b82ee204697a59d8882698923d16314acbe0e9b4df90bff9a9fc
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10.6` - linux; amd64

```console
$ docker pull julia@sha256:3aeafe8fef111e7073cb229623e822507822ab70ff032754f9bcd283a54fcc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211472178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba19a7a93cc178c1b065587a36e67da518fc48ff05e9300fc4d8a2027b18a9aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101adee98773e3e59fecdd887e2522c82747a6adcc91a254babc8ce166f83ada`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.7 MB (5713103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694fa0b0ac731e838a9379e1e4838cd0364ec17b215749e0494fd8364a01f18e`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 176.6 MB (176630711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b576fe205428e7457a4c4b9a480e81d65ccbff53d0d1aa12db2467b42b4d0`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:541a7abe5faf1739d10f182a28771ab86be8af1894a4319028284f9d4cf314e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20e8b60a2df1079f8a8fedaed593057da563b14c0bc4ac765f25c79d8ea0339`

```dockerfile
```

-	Layers:
	-	`sha256:2cb25d4138f2051c814b62f70099ef0fedeaf9c5f9b977d30f4d6d7ac8bd5ca3`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4be31bf4d664270127ffb78183e4abbbe8992903b096c010cf68e6473b6368`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:550f700ca18814aeb60a14bb3305385d3cebaf7b5db8a304fb4a2f8afdbca53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212043012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c31b68e3daba85eed82a663f11cdde057281b90fc7dc5576da4400849a5af3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94441d0ec70e24000d147d731879b8df09a90ade89414c00807401b585a4e344`  
		Last Modified: Tue, 12 Nov 2024 03:18:38 GMT  
		Size: 177.3 MB (177347250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dca3138d75dc5371de1d1506ac0e841b70132e76afd01bb4aa461c7dae441c`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:bd869a20569dbd9d256f228792d771507a079add37d7b8351546ba13aa98a6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34912f0906fc1e30b25afd6907d7fc970164e36b5362e726b27aa582d98ba18e`

```dockerfile
```

-	Layers:
	-	`sha256:52507a8bb01386617e76c7187069f4c817faf2c4f5eb45aa59ec1ee73e17844e`  
		Last Modified: Tue, 12 Nov 2024 03:18:34 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ecd40236b77b231ee24deb064bd5829a27583c167bb1943564c6913e4c7953`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - linux; 386

```console
$ docker pull julia@sha256:98c7a03e63cb4f4cc2581ea02fb1b1d015975e79db925da1cefcca3bbd74ab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193830763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916290621e529687cf43d50c0afcd5530885dc5d973278312158823e42fc4703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ccc2160ddf2d5a1ac2fd82f045731436b933d62a3567dc56ae446444246242`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 5.9 MB (5872110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae64e8c9c17e01b02c497d969bdd711fb52a21dc8dad450d92682337b67a7a`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 157.8 MB (157812833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b977eea4fa680c3b916e318a0d110cd539eb781779cfbb3792dba448d2778f`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:51c21a7faf1c686471eb59db5c1602aeaa52a33a6e23bc9fb675ad9708c26fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961459d1515bf19e1a9906c4e850c146bacf5b24b5190e09ec5d6f3aade67fcd`

```dockerfile
```

-	Layers:
	-	`sha256:ed8bc43d2238533bc2b97d27212c368e9a6e3745ee4733c4f17b536bd4d8f78c`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ca5c79fea5ce39612993be9346f6b7f5d5eb7f8c0b1058535c1ae7fed85a1`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - linux; ppc64le

```console
$ docker pull julia@sha256:058d6048f5793495308f357bb305111bbd44713a6c92a9622df3e33fb32d0b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194682502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ec0f27255c38e1d25b100b57c80831baf5e7ae1e4cea3f7f254bd311c979fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5380f0969ba018b5e9f1ac8bc89d2c882dfc6f5713b4b32c3d01095483ad1f50`  
		Last Modified: Tue, 12 Nov 2024 02:56:00 GMT  
		Size: 155.3 MB (155307474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862ed6b3b616f194106cdb7ea8f1eb67b7600de9bb7d0dbb07e1928ce342945`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6` - unknown; unknown

```console
$ docker pull julia@sha256:aa36ec2e15282e201e9cab59e959865294c2620546e9a3caace21ade5d1857a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a851761cbac62b422c180a6540db2ed4146b483f62de584e6594226776586b5`

```dockerfile
```

-	Layers:
	-	`sha256:91f6db47e4d73faa28d3f003c755567b4ab5fce431b1e0b85d090ae464a6e991`  
		Last Modified: Tue, 12 Nov 2024 02:55:56 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ecdd39defabd1d11dfc2310ab08e80a419ffb0ed4406938cded9e7fcb4d765`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.6` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6-alpine`

```console
$ docker pull julia@sha256:f3973ab4ab6ef3b0f3f095a68a1e50dd2a0bf3884fa06b3cc60f49ba33cded14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.6-alpine` - linux; amd64

```console
$ docker pull julia@sha256:9812c83d818e41abd04df2b7cb5d963c24bbdb25bd098c02b5f0284f4a073277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b209bbb5f468c1fb71e00fbdeec0249a4fd34c0afea421a6327f37f9b81ed488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b151b060aa63746dd750e670ea5bdc1620a2092ab16549d04dcfa0a35be99a19`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 179.2 MB (179208171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b5fa518dc4207c412f265ae78a462120f7d1ca4429f61b221a864bd2ae4767`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:f1676098e123ba7b82a858b8f167109a730cd1eb3794682717776678add6ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 KB (86826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f0fa775c45dff7002ab8e42f1072159d5d435f423346b1b63f3ac42be509b`

```dockerfile
```

-	Layers:
	-	`sha256:0a7594e53064d03d5a486067821d62a0fe2806e32e1945dac733e9bec7712bb5`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e78df92e975c56c25b51babfa966c91cd333817b0d41a2ab67bd3ebcade3ead1`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-alpine3.19`

```console
$ docker pull julia@sha256:03c9c31d6a720ea5ddf62e6f4179fa6c78b1443577b48ea6808f2c7e756d8b01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.6-alpine3.19` - linux; amd64

```console
$ docker pull julia@sha256:accaafcfbbb155631e4a5174306213b4b5e414684bdebf6338565a73df9d866f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182628335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb22a575f4823a0b6af31c76a9ee92b9d07747b074ffcea98593d32b6fdae70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff76342ab75aef9ffda7369b4499fea8ac40f04447dcb223287661da9c8805ea`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 179.2 MB (179208239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11cad05def77ae3f6ffa5a1536823eececb770333a073dbcc5616867b69582b3`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-alpine3.19` - unknown; unknown

```console
$ docker pull julia@sha256:412190df9c13b55eebe439aaa4359ac6589fa3aee0f29991f5ce7450137d5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 KB (89829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc08707821bbb23fe9bcbdd0357d465f40ae145d2f9930bb51672aa9c4a7d2a`

```dockerfile
```

-	Layers:
	-	`sha256:1cde15cb7c60ddac05cf3811e6a1f4326078328ce01b5cb2f2b04eaf452f01d9`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc582427fb65f80fe5a33c625e31ca63117ad4b103b38bcbdefaf8179ff8a8f`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 12.0 KB (11964 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-alpine3.20`

```console
$ docker pull julia@sha256:f3973ab4ab6ef3b0f3f095a68a1e50dd2a0bf3884fa06b3cc60f49ba33cded14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.6-alpine3.20` - linux; amd64

```console
$ docker pull julia@sha256:9812c83d818e41abd04df2b7cb5d963c24bbdb25bd098c02b5f0284f4a073277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182832441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b209bbb5f468c1fb71e00fbdeec0249a4fd34c0afea421a6327f37f9b81ed488`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.6-musl-x86_64.tar.gz'; 			sha256='ce413fb11de97efe8dbe4f3c57dc44741832e3a4a4187e1da590c16a4742c307'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b151b060aa63746dd750e670ea5bdc1620a2092ab16549d04dcfa0a35be99a19`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 179.2 MB (179208171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b5fa518dc4207c412f265ae78a462120f7d1ca4429f61b221a864bd2ae4767`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-alpine3.20` - unknown; unknown

```console
$ docker pull julia@sha256:f1676098e123ba7b82a858b8f167109a730cd1eb3794682717776678add6ebca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 KB (86826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f0fa775c45dff7002ab8e42f1072159d5d435f423346b1b63f3ac42be509b`

```dockerfile
```

-	Layers:
	-	`sha256:0a7594e53064d03d5a486067821d62a0fe2806e32e1945dac733e9bec7712bb5`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 74.2 KB (74246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e78df92e975c56c25b51babfa966c91cd333817b0d41a2ab67bd3ebcade3ead1`  
		Last Modified: Tue, 12 Nov 2024 02:03:17 GMT  
		Size: 12.6 KB (12580 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-bookworm`

```console
$ docker pull julia@sha256:333b4a42171023dfc8fed32aec4d45504596f86686d5975710edcc29dc1b6555
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

### `julia:1.10.6-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:3aeafe8fef111e7073cb229623e822507822ab70ff032754f9bcd283a54fcc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211472178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba19a7a93cc178c1b065587a36e67da518fc48ff05e9300fc4d8a2027b18a9aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101adee98773e3e59fecdd887e2522c82747a6adcc91a254babc8ce166f83ada`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.7 MB (5713103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694fa0b0ac731e838a9379e1e4838cd0364ec17b215749e0494fd8364a01f18e`  
		Last Modified: Tue, 12 Nov 2024 02:03:22 GMT  
		Size: 176.6 MB (176630711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95b576fe205428e7457a4c4b9a480e81d65ccbff53d0d1aa12db2467b42b4d0`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:541a7abe5faf1739d10f182a28771ab86be8af1894a4319028284f9d4cf314e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20e8b60a2df1079f8a8fedaed593057da563b14c0bc4ac765f25c79d8ea0339`

```dockerfile
```

-	Layers:
	-	`sha256:2cb25d4138f2051c814b62f70099ef0fedeaf9c5f9b977d30f4d6d7ac8bd5ca3`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2449212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4be31bf4d664270127ffb78183e4abbbe8992903b096c010cf68e6473b6368`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 17.2 KB (17214 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:550f700ca18814aeb60a14bb3305385d3cebaf7b5db8a304fb4a2f8afdbca53a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.0 MB (212043012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c31b68e3daba85eed82a663f11cdde057281b90fc7dc5576da4400849a5af3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94441d0ec70e24000d147d731879b8df09a90ade89414c00807401b585a4e344`  
		Last Modified: Tue, 12 Nov 2024 03:18:38 GMT  
		Size: 177.3 MB (177347250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dca3138d75dc5371de1d1506ac0e841b70132e76afd01bb4aa461c7dae441c`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:bd869a20569dbd9d256f228792d771507a079add37d7b8351546ba13aa98a6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2465597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34912f0906fc1e30b25afd6907d7fc970164e36b5362e726b27aa582d98ba18e`

```dockerfile
```

-	Layers:
	-	`sha256:52507a8bb01386617e76c7187069f4c817faf2c4f5eb45aa59ec1ee73e17844e`  
		Last Modified: Tue, 12 Nov 2024 03:18:34 GMT  
		Size: 2.4 MB (2448264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1ecd40236b77b231ee24deb064bd5829a27583c167bb1943564c6913e4c7953`  
		Last Modified: Tue, 12 Nov 2024 03:18:33 GMT  
		Size: 17.3 KB (17333 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bookworm` - linux; 386

```console
$ docker pull julia@sha256:98c7a03e63cb4f4cc2581ea02fb1b1d015975e79db925da1cefcca3bbd74ab44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193830763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916290621e529687cf43d50c0afcd5530885dc5d973278312158823e42fc4703`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ccc2160ddf2d5a1ac2fd82f045731436b933d62a3567dc56ae446444246242`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 5.9 MB (5872110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ae64e8c9c17e01b02c497d969bdd711fb52a21dc8dad450d92682337b67a7a`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 157.8 MB (157812833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b977eea4fa680c3b916e318a0d110cd539eb781779cfbb3792dba448d2778f`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:51c21a7faf1c686471eb59db5c1602aeaa52a33a6e23bc9fb675ad9708c26fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961459d1515bf19e1a9906c4e850c146bacf5b24b5190e09ec5d6f3aade67fcd`

```dockerfile
```

-	Layers:
	-	`sha256:ed8bc43d2238533bc2b97d27212c368e9a6e3745ee4733c4f17b536bd4d8f78c`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 2.4 MB (2446304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921ca5c79fea5ce39612993be9346f6b7f5d5eb7f8c0b1058535c1ae7fed85a1`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 17.2 KB (17179 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:058d6048f5793495308f357bb305111bbd44713a6c92a9622df3e33fb32d0b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194682502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ec0f27255c38e1d25b100b57c80831baf5e7ae1e4cea3f7f254bd311c979fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5380f0969ba018b5e9f1ac8bc89d2c882dfc6f5713b4b32c3d01095483ad1f50`  
		Last Modified: Tue, 12 Nov 2024 02:56:00 GMT  
		Size: 155.3 MB (155307474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4862ed6b3b616f194106cdb7ea8f1eb67b7600de9bb7d0dbb07e1928ce342945`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:aa36ec2e15282e201e9cab59e959865294c2620546e9a3caace21ade5d1857a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a851761cbac62b422c180a6540db2ed4146b483f62de584e6594226776586b5`

```dockerfile
```

-	Layers:
	-	`sha256:91f6db47e4d73faa28d3f003c755567b4ab5fce431b1e0b85d090ae464a6e991`  
		Last Modified: Tue, 12 Nov 2024 02:55:56 GMT  
		Size: 2.5 MB (2452397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95ecdd39defabd1d11dfc2310ab08e80a419ffb0ed4406938cded9e7fcb4d765`  
		Last Modified: Tue, 12 Nov 2024 02:55:55 GMT  
		Size: 17.3 KB (17260 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-bullseye`

```console
$ docker pull julia@sha256:87d036e9f4482746e413fc698cd0dc5d882a7919a25668256802a0cc230037a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.10.6-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:9da1a5e74843f16f44629dd2e49761cbb851fefff24b0a6aa2b7039725db2617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210305686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f741341a68cfddfdeeb50bc6d743cdea87dbc97d03305e9616ab842dd9c198bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948cbffd20e08d7cd6e8bc9a1ac4ed59b132379617b89e0f98e1e06d8df494c9`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 2.2 MB (2222782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bd109eef3e4613b36ea2b28d1f9e6c658d5f29939d7fbd68fe2484fe1dca42`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 176.6 MB (176630975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a826e971f361c507a3a036b2a2173a1b322902e9c82da4f3c8c301a1538b54`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:9f88dcf84d296911034b1ff03020ba556ce8b682d7d60c826b2659529db4f65d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce9d2aa083e280cf947dab6cf89134ff957a48ca67656363fa6e472f8bb83bf`

```dockerfile
```

-	Layers:
	-	`sha256:768498f76dc4f302a83c727a37712a9e7ee842e5870fb8cf1646d17bbfced199`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 2.7 MB (2717653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54035c10a2e7fc4dafa6c5e78136f1cefedf66c89b6435957574c8794d2091f4`  
		Last Modified: Tue, 12 Nov 2024 02:03:23 GMT  
		Size: 16.6 KB (16626 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:e433c30dd4b33f9abcb1f281c4c3f39fe63149880256684d614d47c9e90c933b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209649976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20e6926fff5d295e4d315640ebcce594cd97602ce1a518e7df54a2c30ea852`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d503ab39ed3cdd3f8d0a29b0b3ee1941169aba3493d0ccb5ea9ff12821b3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.2 MB (2210272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d2f4cb45ddcafd38f0bf2b839ff651a82cae793f523a9b9c94d92f92f0ac35`  
		Last Modified: Tue, 12 Nov 2024 03:19:41 GMT  
		Size: 177.3 MB (177347738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3241f2572494099db877cd9559471aa5083ebfbcd02fd7669bc87b0ae383ed`  
		Last Modified: Tue, 12 Nov 2024 03:19:36 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:3390fae85a2ed3976607582c363d23a5f473c2efece8327c5d63b0402a527a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2733390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:556b34c046c2408945e1713ca31a0f6ebdaf8d12c5b65f295415e7c2ae532f24`

```dockerfile
```

-	Layers:
	-	`sha256:2e0778fd08b654e9a4d6bba8ed048b8a6262f281260d7c06da239e310ede3bdf`  
		Last Modified: Tue, 12 Nov 2024 03:19:36 GMT  
		Size: 2.7 MB (2716669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:458e274b5701a0ba44c9d646f415a1394f928aaf9f67d7f9c4ba14e998ff829f`  
		Last Modified: Tue, 12 Nov 2024 03:19:36 GMT  
		Size: 16.7 KB (16721 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.6-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2f5bf29934557f3fe5f20df7d3fda714f46ab7d00d1d78563da5ce2ea1347d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192565376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d760b242e12ae38909bbdf7ac1e4894db86b0f44efbad49f0d5730bafdd259d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 28 Oct 2024 23:59:11 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["bash"]
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 28 Oct 2024 23:59:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 28 Oct 2024 23:59:11 GMT
ENV JULIA_VERSION=1.10.6
# Mon, 28 Oct 2024 23:59:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.6-linux-x86_64.tar.gz'; 			sha256='8b53429e17585c66476b39f2b2279da207ea0f310c55db38f3410bdd4f6a3d49'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.6-linux-aarch64.tar.gz'; 			sha256='5530359839544ba1ee8f6f66728fd4f9b591822c1633f93cf9672c7f9528fc3a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.6-linux-i686.tar.gz'; 			sha256='52771086511905c22669bc8667a98a97ad26e82747a429165fde2641672e962b'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.6-linux-ppc64le.tar.gz'; 			sha256='bbfd63ba2bf497f82101ef8ca3e681adca4ab95f9d5e12abfb2cf3a3c72d6126'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 28 Oct 2024 23:59:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Oct 2024 23:59:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed931e316242f942722ef7ebad630dd0cd42027c2f4415b19818833a3c2c9ec2`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.3 MB (2328131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add27b5406614d2e30c2e8ac830174651bc23c09cd51700a5131d706f269a7b7`  
		Last Modified: Tue, 12 Nov 2024 02:03:24 GMT  
		Size: 157.8 MB (157813525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aaa6432cf1844f28cfb2c33197977a66eeef33d48ca3c6994801c0abc58d3f0`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.6-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:4f20694f7a6d3701cd66522fd54c45df571d0b55e1b3710431a4d667257d1d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13760d469cd1d8b7d0549cfa94236f381957c64830bf3048819a00d136f0aee`

```dockerfile
```

-	Layers:
	-	`sha256:9c92b2c816d747ff699a1984d3f7d27ffa25765dd8e1851f4755984e5edca047`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.7 MB (2714761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62291fccea8724347aca3fc10604cb54ac99007d5cb9f45042010064387a07a2`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.6-windowsservercore`

```console
$ docker pull julia@sha256:bad5fd470043108972fab03ab7fba19dd1a37e13481871a96cfaccc0c9a78304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10.6-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.6-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:58087ae2d9648fa6b36d657e915e543117eeae1bb7dd7ecd19ab015510e67d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.10.6-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:6ca14732d9b63fca4b7397eadd040a3c87ccd84e1ba749fb7e1ee9bc42244913
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090791615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d349843745bd27b77509eb661965f36217fa3b818dd96f5ef8ad5d5c868c8d93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Tue, 29 Oct 2024 22:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 22:58:31 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 22:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 22:58:33 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:00:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:00:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187f98b1f55258e314fedb9c2f6226e1c2a11740febbd0ce89d238e43c0bed2`  
		Last Modified: Tue, 29 Oct 2024 23:00:43 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0606836b66ce8f497eac48f690ee807b532d6777b4e56ce704dd15e77e678a`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9b820753126ccfc32f3fba865e5d5b4824aedcdaf3831831d2844d43d919f6`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed0726905f5fbf316e8c8c6741bc1793dde3958dca4f53a28ff39972d4253b31`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eff14262dc220189629e33a16987149944ad23b1b5f939113fa634c51f7f4b`  
		Last Modified: Tue, 29 Oct 2024 23:01:04 GMT  
		Size: 189.0 MB (188959879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a37e9e4b5cd836f0416d006af1817bf06ea1be011782932bf2b3785e6a08c44`  
		Last Modified: Tue, 29 Oct 2024 23:00:41 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0e65c00e6c1db3fd045c6a7adc21172ef95b4163656cc090fe6155b59939459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.10.6-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:0e742f15776e4f7e2466446691d4e7d0ae81576fea07e6ac69eea39d103d0173
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1988310186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3085046212c05c9e4b0a731e38e30128a7ac793956c2995e4417d66e1888e4b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Tue, 29 Oct 2024 23:56:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 29 Oct 2024 23:56:59 GMT
ENV JULIA_VERSION=1.10.6
# Tue, 29 Oct 2024 23:57:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.6-win64.exe
# Tue, 29 Oct 2024 23:57:02 GMT
ENV JULIA_SHA256=f29e62ea3edede6b9a245ca1117d5f5232a78f324902a69368e3ed5836f96d59
# Tue, 29 Oct 2024 23:59:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 29 Oct 2024 23:59:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a703ec8db6afe2491ab0518ad479df3ea9eb52d5967771bcebf035a59b29d6`  
		Last Modified: Tue, 29 Oct 2024 23:59:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8738f7e52db049fd38af00a87bd6e9119f5abbd70ab1bd552a1f01f9785c6b5d`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0083b70e021328f6ae7e9d213e77735279f1cf457c243584e8cea8bad89d18`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220778260973a205a267336a441e793360c94d727e8fce10de071e7edb0fa48b`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc4ea8989979e5b3bdf5bafb635c0dd5f91c792a52a23c77f353466f2dbeea3`  
		Last Modified: Tue, 29 Oct 2024 23:59:50 GMT  
		Size: 189.0 MB (188962205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ae0a51fc94fd2d69da5be3323e71e7737e28dd291e65c140e1836658098af0`  
		Last Modified: Tue, 29 Oct 2024 23:59:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:5cf1f32cf1d3836ff87a0614efb58e7c7ec84ca3fa6785efc317e19154cfded0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:46803c478e2350ee2ec92eb18c58b172064acc26b43ddbd6739173173758bf99
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
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-bullseye`

```console
$ docker pull julia@sha256:ec93afc7220f9a01c0b7f50a5fff3e7fcfe8edbbcac52c005cf79267185dcd1b
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
$ docker pull julia@sha256:6ad1f47f6bb14abd9094fbe7ac2f7e8713922b08f8bc167b527b2403ac32c3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290772899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cf8d3dc0fc2427f42f0cf27f89a7328b49f7cc84ae385e42505875d60b118`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90e228fdb2b7decf92841af0c19add44ea11f38fcccc06b67e0c351d0c0f53`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.2 MB (2222723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5ad4ee1a7abf803e6947c14b525b93e982ced55a5c28f8e01d8d0d91274c2f`  
		Last Modified: Tue, 12 Nov 2024 02:03:46 GMT  
		Size: 257.1 MB (257098246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4bd9a096e04ad4efce79ea96e89ab73d28e939ea033cdf4cdeb09371c39b8a`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e84cbbdf7a63dcee3e8f8a6eb5f72fc71e8c852aa4bee18c2470630e521e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9102b91fab566df758f1323e7f62fd57b103df327c4c2691548fe70edd2b8a13`

```dockerfile
```

-	Layers:
	-	`sha256:8b29c2f1c5db4ecd50d839c3a0fbac2f2a2939dcd6a57dd3bd99143eab64afa5`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.7 MB (2717035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57de41a80224d8c0897e41e665d25ee9ad4ae7344f650f87a23a3f3cb5fdd2c8`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6f833498ed7451c126fc9114e09c938071fcdc172068faa9c07621b498bf1e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286308812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c83668c2dc30778d6eb47e259cd5798cbd50fef427f433f63feccb51126666`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d503ab39ed3cdd3f8d0a29b0b3ee1941169aba3493d0ccb5ea9ff12821b3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.2 MB (2210272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb865f98aa3d1aa03080b347b6b4951da76e34c127c12b3ad122ee6ae788de66`  
		Last Modified: Tue, 12 Nov 2024 03:17:28 GMT  
		Size: 254.0 MB (254006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192e63792f6ee32a588d7580f44fd2dd8213eb64be51dfa38e4d06e2c08b45b`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cc59ebca35370f7217603a1df7120b5f5712900f31318bcba7c1289fbed5f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318ae46fdd8c646ad00da5ba9754f2f9209887473826a38e000cf260ca282e8`

```dockerfile
```

-	Layers:
	-	`sha256:5a79359a4ca09a47591c34ca139874ad937e3ef4fcfe00f8b027fc309d959563`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.7 MB (2717297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031b66b179eb4d2ca81bcc90cf94668aeff3314707742239d0036d0fea1018e3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2928e66b6e739ba1a7677026582e0dcb011a56b214b521ada383940e5c9e1853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269410481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4477a6226df30b1aee6fbf7bf27dd29b1a5d6ed67f0861f3daaa9de2239a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d452f6a4c4aebe891a7d111deaa15df8668219b2dcf00736127fee1208a5e0d`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.3 MB (2328167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daaec2aac82defed7f37a975c8ed6547bf042c092d9660c50d3b9e07cdf58e0`  
		Last Modified: Tue, 12 Nov 2024 02:03:34 GMT  
		Size: 234.7 MB (234658597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7226831f566cb96842ea556ee18df519c2b14c3a30976f87f6eeb967085b6`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2aa198ddc7916c5b5315ef43ffccc612a5cc2a49b8743c02ded0b47eeeffb17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1de9bbadaed9fdfd49e994f78e3429dcc4cce152e0b8031fda2c978eb074eef`

```dockerfile
```

-	Layers:
	-	`sha256:3851f1a748150fe57188c5c8c5cfe69d2756c1b7e0433e5942d029ae64c69f77`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.7 MB (2714133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10734275766cf0df9be09554590c38267f13e935a48a61525fe313c7fb353429`  
		Last Modified: Tue, 12 Nov 2024 02:03:28 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1`

```console
$ docker pull julia@sha256:5cf1f32cf1d3836ff87a0614efb58e7c7ec84ca3fa6785efc317e19154cfded0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11.1` - linux; amd64

```console
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.1` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-bookworm`

```console
$ docker pull julia@sha256:46803c478e2350ee2ec92eb18c58b172064acc26b43ddbd6739173173758bf99
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

### `julia:1.11.1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.1-bullseye`

```console
$ docker pull julia@sha256:ec93afc7220f9a01c0b7f50a5fff3e7fcfe8edbbcac52c005cf79267185dcd1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.11.1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:6ad1f47f6bb14abd9094fbe7ac2f7e8713922b08f8bc167b527b2403ac32c3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290772899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cf8d3dc0fc2427f42f0cf27f89a7328b49f7cc84ae385e42505875d60b118`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90e228fdb2b7decf92841af0c19add44ea11f38fcccc06b67e0c351d0c0f53`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.2 MB (2222723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5ad4ee1a7abf803e6947c14b525b93e982ced55a5c28f8e01d8d0d91274c2f`  
		Last Modified: Tue, 12 Nov 2024 02:03:46 GMT  
		Size: 257.1 MB (257098246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4bd9a096e04ad4efce79ea96e89ab73d28e939ea033cdf4cdeb09371c39b8a`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e84cbbdf7a63dcee3e8f8a6eb5f72fc71e8c852aa4bee18c2470630e521e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9102b91fab566df758f1323e7f62fd57b103df327c4c2691548fe70edd2b8a13`

```dockerfile
```

-	Layers:
	-	`sha256:8b29c2f1c5db4ecd50d839c3a0fbac2f2a2939dcd6a57dd3bd99143eab64afa5`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.7 MB (2717035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57de41a80224d8c0897e41e665d25ee9ad4ae7344f650f87a23a3f3cb5fdd2c8`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6f833498ed7451c126fc9114e09c938071fcdc172068faa9c07621b498bf1e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286308812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c83668c2dc30778d6eb47e259cd5798cbd50fef427f433f63feccb51126666`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d503ab39ed3cdd3f8d0a29b0b3ee1941169aba3493d0ccb5ea9ff12821b3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.2 MB (2210272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb865f98aa3d1aa03080b347b6b4951da76e34c127c12b3ad122ee6ae788de66`  
		Last Modified: Tue, 12 Nov 2024 03:17:28 GMT  
		Size: 254.0 MB (254006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192e63792f6ee32a588d7580f44fd2dd8213eb64be51dfa38e4d06e2c08b45b`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cc59ebca35370f7217603a1df7120b5f5712900f31318bcba7c1289fbed5f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318ae46fdd8c646ad00da5ba9754f2f9209887473826a38e000cf260ca282e8`

```dockerfile
```

-	Layers:
	-	`sha256:5a79359a4ca09a47591c34ca139874ad937e3ef4fcfe00f8b027fc309d959563`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.7 MB (2717297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031b66b179eb4d2ca81bcc90cf94668aeff3314707742239d0036d0fea1018e3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:2928e66b6e739ba1a7677026582e0dcb011a56b214b521ada383940e5c9e1853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269410481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4477a6226df30b1aee6fbf7bf27dd29b1a5d6ed67f0861f3daaa9de2239a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d452f6a4c4aebe891a7d111deaa15df8668219b2dcf00736127fee1208a5e0d`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.3 MB (2328167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daaec2aac82defed7f37a975c8ed6547bf042c092d9660c50d3b9e07cdf58e0`  
		Last Modified: Tue, 12 Nov 2024 02:03:34 GMT  
		Size: 234.7 MB (234658597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7226831f566cb96842ea556ee18df519c2b14c3a30976f87f6eeb967085b6`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.1-bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2aa198ddc7916c5b5315ef43ffccc612a5cc2a49b8743c02ded0b47eeeffb17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1de9bbadaed9fdfd49e994f78e3429dcc4cce152e0b8031fda2c978eb074eef`

```dockerfile
```

-	Layers:
	-	`sha256:3851f1a748150fe57188c5c8c5cfe69d2756c1b7e0433e5942d029ae64c69f77`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.7 MB (2714133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10734275766cf0df9be09554590c38267f13e935a48a61525fe313c7fb353429`  
		Last Modified: Tue, 12 Nov 2024 02:03:28 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.1-windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11.1-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.1-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:1.11.1-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:1.11.1-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:46803c478e2350ee2ec92eb18c58b172064acc26b43ddbd6739173173758bf99
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
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:bullseye`

```console
$ docker pull julia@sha256:ec93afc7220f9a01c0b7f50a5fff3e7fcfe8edbbcac52c005cf79267185dcd1b
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
$ docker pull julia@sha256:6ad1f47f6bb14abd9094fbe7ac2f7e8713922b08f8bc167b527b2403ac32c3a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290772899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873cf8d3dc0fc2427f42f0cf27f89a7328b49f7cc84ae385e42505875d60b118`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df90e228fdb2b7decf92841af0c19add44ea11f38fcccc06b67e0c351d0c0f53`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.2 MB (2222723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5ad4ee1a7abf803e6947c14b525b93e982ced55a5c28f8e01d8d0d91274c2f`  
		Last Modified: Tue, 12 Nov 2024 02:03:46 GMT  
		Size: 257.1 MB (257098246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4bd9a096e04ad4efce79ea96e89ab73d28e939ea033cdf4cdeb09371c39b8a`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:8e84cbbdf7a63dcee3e8f8a6eb5f72fc71e8c852aa4bee18c2470630e521e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9102b91fab566df758f1323e7f62fd57b103df327c4c2691548fe70edd2b8a13`

```dockerfile
```

-	Layers:
	-	`sha256:8b29c2f1c5db4ecd50d839c3a0fbac2f2a2939dcd6a57dd3bd99143eab64afa5`  
		Last Modified: Tue, 12 Nov 2024 02:03:41 GMT  
		Size: 2.7 MB (2717035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57de41a80224d8c0897e41e665d25ee9ad4ae7344f650f87a23a3f3cb5fdd2c8`  
		Last Modified: Tue, 12 Nov 2024 02:03:40 GMT  
		Size: 17.2 KB (17230 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6f833498ed7451c126fc9114e09c938071fcdc172068faa9c07621b498bf1e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286308812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c83668c2dc30778d6eb47e259cd5798cbd50fef427f433f63feccb51126666`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd6d503ab39ed3cdd3f8d0a29b0b3ee1941169aba3493d0ccb5ea9ff12821b3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.2 MB (2210272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb865f98aa3d1aa03080b347b6b4951da76e34c127c12b3ad122ee6ae788de66`  
		Last Modified: Tue, 12 Nov 2024 03:17:28 GMT  
		Size: 254.0 MB (254006569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192e63792f6ee32a588d7580f44fd2dd8213eb64be51dfa38e4d06e2c08b45b`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:cc59ebca35370f7217603a1df7120b5f5712900f31318bcba7c1289fbed5f906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2734646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318ae46fdd8c646ad00da5ba9754f2f9209887473826a38e000cf260ca282e8`

```dockerfile
```

-	Layers:
	-	`sha256:5a79359a4ca09a47591c34ca139874ad937e3ef4fcfe00f8b027fc309d959563`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 2.7 MB (2717297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:031b66b179eb4d2ca81bcc90cf94668aeff3314707742239d0036d0fea1018e3`  
		Last Modified: Tue, 12 Nov 2024 03:17:22 GMT  
		Size: 17.3 KB (17349 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:2928e66b6e739ba1a7677026582e0dcb011a56b214b521ada383940e5c9e1853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269410481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a4477a6226df30b1aee6fbf7bf27dd29b1a5d6ed67f0861f3daaa9de2239a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aea24d0416284c8bc498d91bac1c90e2bf12b01e7867f799161bbb874a8323b`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 32.4 MB (32423351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d452f6a4c4aebe891a7d111deaa15df8668219b2dcf00736127fee1208a5e0d`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.3 MB (2328167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daaec2aac82defed7f37a975c8ed6547bf042c092d9660c50d3b9e07cdf58e0`  
		Last Modified: Tue, 12 Nov 2024 02:03:34 GMT  
		Size: 234.7 MB (234658597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7226831f566cb96842ea556ee18df519c2b14c3a30976f87f6eeb967085b6`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bullseye` - unknown; unknown

```console
$ docker pull julia@sha256:2aa198ddc7916c5b5315ef43ffccc612a5cc2a49b8743c02ded0b47eeeffb17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2731327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1de9bbadaed9fdfd49e994f78e3429dcc4cce152e0b8031fda2c978eb074eef`

```dockerfile
```

-	Layers:
	-	`sha256:3851f1a748150fe57188c5c8c5cfe69d2756c1b7e0433e5942d029ae64c69f77`  
		Last Modified: Tue, 12 Nov 2024 02:03:29 GMT  
		Size: 2.7 MB (2714133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10734275766cf0df9be09554590c38267f13e935a48a61525fe313c7fb353429`  
		Last Modified: Tue, 12 Nov 2024 02:03:28 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:5cf1f32cf1d3836ff87a0614efb58e7c7ec84ca3fa6785efc317e19154cfded0
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
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:64e1a5afebbb6d82a2063bb266067af3a52d74fa86d0547b8521fa2cd7ce7052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.9 MB (291939491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7efdf20fceef131da3a15e84f2c8b9fab1fb399aedf8acfaa6e4189a4b0aad5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ad492139ae6bbe92c2096b4ea224cb2f92d1bf70d43f908ae2b46a8791db95`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 5.7 MB (5713106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3463d1b4a38c3e35b01004ebbfde1c4657940e71786b0e52ee32efc70a2f917c`  
		Last Modified: Tue, 12 Nov 2024 02:03:31 GMT  
		Size: 257.1 MB (257098024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed010d60254da044064957a14aaaa5800a5a9745edea6ef98c9c104b963e5c`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:16b4241bf41927ec35b7adf8fd0f0bbe42d830d1ed414de30e4a22f9a6058773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4f1d04d196952e25d5f1e53cea2313148f32d7248265344c6e7b23875f545a`

```dockerfile
```

-	Layers:
	-	`sha256:aefbe1edf51e774224c6d1e7ffd0edc0df189a35917547ade3d01fbc10489b57`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 2.4 MB (2449176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beacd3d8253e9f5cc3f389306869521fd92b5dfa1f534516c593a56c9c7998fd`  
		Last Modified: Tue, 12 Nov 2024 02:03:27 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b9c41abbfdbca1e23173bdb8475680dbef574df5582f85784e16373b4302d79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.7 MB (288702621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d966a57636e40c1c4b4d52c008dbb5048fd6fbfb6b66a8dcbdbe8caac64e3a16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69c1ab2cc429374c52d1e70aa53ad1bf86d18fcbd496a997a0dca437692b0ef`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 5.5 MB (5538037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dbf448eb314be708dc557a75e20b05e2b6bd4c73634deb8166ca095023013e`  
		Last Modified: Tue, 12 Nov 2024 03:16:03 GMT  
		Size: 254.0 MB (254006856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae98e9cd8637a4e0ac604e9d78c397cb9802e7964ed757cc027cf9687471c5b`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:3d383eb8f77ecea1009dce895c62d7cd8d941e27c834539b5dc9987de1869bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a0ebf1560f2507a03794889c35180c5612dc125615808029a12a30f23c1688`

```dockerfile
```

-	Layers:
	-	`sha256:3f799c6788d9f9084bd32dfa7b5c8e5156dba60f5e312517a566e4780279d619`  
		Last Modified: Tue, 12 Nov 2024 03:15:58 GMT  
		Size: 2.4 MB (2449498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e131f4e418fb87813af80353b631ed1c7573e8c99512f6f73d28530a5ee90a`  
		Last Modified: Tue, 12 Nov 2024 03:15:57 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:39378a010671403a180c0d38ebce56abef22e8023d349fa36898d578a23a380d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270675572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa8bd36b8c041924f45cf0e3cd6d250106173d67a6d5bb2bb5cb715a5ee4f29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d71791c3c3b110caa5765aa598b285d917b1ab57ac2ac372748210b8e3a1982`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 5.9 MB (5872121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87090019475cb7260427e0fd31cc738adbaadfdd545356131e77c3f5caeda6e`  
		Last Modified: Tue, 12 Nov 2024 02:03:25 GMT  
		Size: 234.7 MB (234657635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73466adaafba1a7190e45ace01e4e282f95a62de28d96c5a9c082200228fa1a9`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:a2826a5f0d238cb8f72e36d211ec4148c308a83f623ba0fa4c7cdfcef1749e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07bd1ae91ae8610393ea5c500ee54b27d91e6beb95b2491222d3cad8208923ce`

```dockerfile
```

-	Layers:
	-	`sha256:f9c01ef87594a55d16b1c5d8fac5e864b1cf9d96f8151c5daba1c5420ffa2a05`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ebd17cf4f0f7a641755da827bff5eb113dbd0733d47902229ffc4368a805822`  
		Last Modified: Tue, 12 Nov 2024 02:03:20 GMT  
		Size: 18.3 KB (18346 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:ec5d24090ff0af8012cf4e4c69a94d424d3643caf119c7b5fff69b67a4fe549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283850150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046993b843c9fa380b825413f918a2a068628fa01a26395eaab8a7f7cfb890d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 16 Oct 2024 17:59:17 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["bash"]
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 16 Oct 2024 17:59:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 16 Oct 2024 17:59:17 GMT
ENV JULIA_VERSION=1.11.1
# Wed, 16 Oct 2024 17:59:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.1-linux-x86_64.tar.gz'; 			sha256='cca8d13dc4507e4f62a129322293313ee574f300d4df9e7db30b7b41c5f8a8f3'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.1-linux-aarch64.tar.gz'; 			sha256='bd623ef3801c5a56103464d349c7901d5cc034405ad289332c67f1e8ecc05840'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.1-linux-i686.tar.gz'; 			sha256='332491f18bb7463635a6f1b2d496b85ff04c5575b6918e02099d5c8ede80546d'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.1-linux-ppc64le.tar.gz'; 			sha256='04e079f5a6565ef2b42b3ecc6b4890efb789a20faba1612227d6b115048bd2cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 17:59:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Oct 2024 17:59:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa879c7e87cbc79a2eb1a2787449c3ae0118bc28aee95fdc9b7cff4bad573de1`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 6.2 MB (6249304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273c33f32173c35524dbc7f936c7a012dcceb451dd63babcda81b5ef19fe189e`  
		Last Modified: Tue, 12 Nov 2024 02:54:07 GMT  
		Size: 244.5 MB (244475122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78883cba72b48756f18c0008df2500c971affd80db06fb1f7a52d6eeb272210`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:1ae06ec6486a65576ccb2c1b049dd8ee145a7a2c5ec1a427dc4b4ce413e712b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5596dc99bdf96f5d442c669501d651c9f2b6cc4cdca46628d16c6f5d5ede6f75`

```dockerfile
```

-	Layers:
	-	`sha256:8c1ab7427cea5a9535f31cb34f1a5fa6e632b9f6419fd06346a015d52819776a`  
		Last Modified: Tue, 12 Nov 2024 02:54:02 GMT  
		Size: 2.5 MB (2453607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a09b453dcd612d4ef853e4bbd4a05cabfbfbc6bb46b8debfccc4748718c237`  
		Last Modified: Tue, 12 Nov 2024 02:54:01 GMT  
		Size: 18.5 KB (18470 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:d36dd547370e9fd68c4f5dc635f8c3ea0da809f71f508a8724c909f927574ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:a114dd8364b3c4135706a0b323f71e0e649bff9cf95ae8300f0378d0951c131e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull julia@sha256:5f7b3fa057a3f34c286a0c29544e30b8e25de7d389fcb9a7c39e5dbc2ac59431
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154909599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73428e1a2c97df8e870d60c63531878514df329661819a1917855fe9c852deb3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 17 Oct 2024 00:04:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:04:47 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:04:48 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:06:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:06:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4316cb4a890d1430c8dbb6f02f1ed4b07cc1f84668ddfe58d132e70173591231`  
		Last Modified: Thu, 17 Oct 2024 00:06:49 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07735f2e4d115dbc648a3fbf628ee5e173125dcd63d695a85f30c2d701668d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf70042980e2e6296807674462b486e411ba5e80ecf7c6ec3bdd5e0e7a5085`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1c8839b71fde8692b035b2f54ea4a7c21650e10ae20680a0ba68b723b9e57d`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4afde2ddc271e774c969b81b72e4ec22aa664487988ca09a851e16930efb47`  
		Last Modified: Thu, 17 Oct 2024 00:07:18 GMT  
		Size: 253.1 MB (253077851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f694e951fd639e6dc35a1e43dce74e5247712830c183397156d8b0ff48747470`  
		Last Modified: Thu, 17 Oct 2024 00:06:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e457f763ca8c5fe3e8a20dd1a3cbf00134231b70f5070b6fa7ce67ff9536e8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull julia@sha256:1aadbfaaaab1ead9b289075e1c50a66c24e73f0abb54ff58987658fb3d721339
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052417149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73d77c77c9074ad1a6ef6af5f3c75625db9c5be5d552e03bdfb712643fa3262`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Thu, 17 Oct 2024 00:07:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 17 Oct 2024 00:07:44 GMT
ENV JULIA_VERSION=1.11.1
# Thu, 17 Oct 2024 00:07:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.1-win64.exe
# Thu, 17 Oct 2024 00:07:46 GMT
ENV JULIA_SHA256=e6b5f4dc2a26ca17087ba31f384a676a4a531b97a2678bcfed3f5786f7e03cd7
# Thu, 17 Oct 2024 00:09:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 17 Oct 2024 00:09:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7310b1b784f497ecef75a191c3fdf858c6c5e7102326517af7e9c8f4a9ba2ab`  
		Last Modified: Thu, 17 Oct 2024 00:09:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f60354745986b41d1c97227046f1bf77a40a1b841e2b733d28d9f336d0517a`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81f4ad3b9ee5bb6c5bcf302663adf9404aed5f2a775c97739ddeaf04c390105`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e95309645bd9402810abb1f62e8d28e2eb50ad30d923ac5635718caafc953f3`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1f65e1c7b97054a3ff76d9eb10192f3ffb9f984e554d5dad56b1deffa4a26e`  
		Last Modified: Thu, 17 Oct 2024 00:09:40 GMT  
		Size: 253.1 MB (253069135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3efcc69a49a46842179fb8d2b256e3aca046c05572afb9537e9e68808da649`  
		Last Modified: Thu, 17 Oct 2024 00:09:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
