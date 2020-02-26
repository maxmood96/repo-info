## `julia:stretch`

```console
$ docker pull julia@sha256:7ede54d2e71425e22670fc8802c60b742a50d721aececa018829edbe8b8f407a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:stretch` - linux; amd64

```console
$ docker pull julia@sha256:412a1465c541adca34ba202b942d2df536b712cea71fc77abc8777a65e4ed1e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.4 MB (133441074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332dae24b1af56c69b02d7819dde8d771ca2fc994baaa370abb980ac812a26fe`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 18:02:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:02:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Feb 2020 18:02:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 18:02:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Feb 2020 18:02:19 GMT
ENV JULIA_VERSION=1.3.1
# Wed, 26 Feb 2020 18:02:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='965c8fab2214f8ce1b3d449d088561a6de61be42543b48c3bbadaed5b02bf824' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 26 Feb 2020 18:02:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb7b6079051ab309e642bc4981419ffcded94c81a3c3b325448174a7b9b2a4b`  
		Last Modified: Wed, 26 Feb 2020 18:05:49 GMT  
		Size: 7.6 MB (7555613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f75aaf5dafa3483a13e53a85f4b62a7ce665bae6af23ed2f3d703a25fae78c3`  
		Last Modified: Wed, 26 Feb 2020 18:06:16 GMT  
		Size: 103.4 MB (103372096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:stretch` - linux; arm variant v7

```console
$ docker pull julia@sha256:7e1318b5ff9de0ccf3c11625b42c2d4b7cd6f8d863034b75f06c8c43785ba36b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119393594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ebc952ed51c62b123b6729fa399d4d3f7152440bedcbd93f4779b0fb9237cc`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Feb 2020 01:01:21 GMT
ADD file:01536f0f2d25f5114e68606280b1a495c4b930ffdd782678b7e8828aef822c14 in / 
# Wed, 26 Feb 2020 01:01:26 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 13:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 13:52:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Feb 2020 13:52:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 13:52:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Feb 2020 13:52:11 GMT
ENV JULIA_VERSION=1.3.1
# Wed, 26 Feb 2020 13:52:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='965c8fab2214f8ce1b3d449d088561a6de61be42543b48c3bbadaed5b02bf824' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 26 Feb 2020 13:52:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e67f89df0287dbfef2de6d9322fee00ab623a93704fcb288963b8d51d7dfffe`  
		Last Modified: Wed, 26 Feb 2020 01:11:47 GMT  
		Size: 19.3 MB (19298348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cde37f4ef89845c34ffbfaa5775572691e1fbc85fcc00bbed273f87ec0af37`  
		Last Modified: Wed, 26 Feb 2020 13:56:11 GMT  
		Size: 6.3 MB (6292004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918bffd96a5efe55aed460abbf7430df80515d5c6379c64da38b65fab98ad0af`  
		Last Modified: Wed, 26 Feb 2020 13:56:57 GMT  
		Size: 93.8 MB (93803242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:stretch` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1ff66cc81906c303d6068336f6ea23d14a976947fcd4a3f88deb0b56ca4873c5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113191822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e22177554d8871c1eb2f59aaecf905c1f467a927eb0dcf8005b1c3348c6cd0`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:58 GMT
ADD file:9a0fcb77e697946112f14ff0a4dfe61aa0be45f648262b8e0be116e289964e4d in / 
# Wed, 26 Feb 2020 00:51:07 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 06:41:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:41:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Feb 2020 06:41:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 06:41:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Feb 2020 06:41:07 GMT
ENV JULIA_VERSION=1.3.1
# Wed, 26 Feb 2020 06:41:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='965c8fab2214f8ce1b3d449d088561a6de61be42543b48c3bbadaed5b02bf824' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 26 Feb 2020 06:41:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:81610314811e98d4dba43f609b410f2d09dbcd135dc4cd4d8293fec3644dbea8`  
		Last Modified: Wed, 26 Feb 2020 00:58:54 GMT  
		Size: 20.4 MB (20369979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477be42a574a5f1078e07d0fbf64809f1fffeda23a2b7726d8ad20713b55b795`  
		Last Modified: Wed, 26 Feb 2020 06:44:56 GMT  
		Size: 6.5 MB (6526692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc98ee74cbf6d638cf9c677b3f68d01ce94656c89b17d2f13dc2a2af7e374c82`  
		Last Modified: Wed, 26 Feb 2020 06:45:20 GMT  
		Size: 86.3 MB (86295151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:stretch` - linux; 386

```console
$ docker pull julia@sha256:70ab08f04aa670946d70eece6e30af03225d46e91a45e35f15746118dbcf610e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130001420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31baf1135f3c915c3261381d1707ae18812c678d14aeee37b2c0a41f45f058da`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 26 Feb 2020 00:35:41 GMT
ADD file:7d77438aab7eb35501c0d27bd4350a3a9b4fd1988ce7e7fc0670a570b3112590 in / 
# Wed, 26 Feb 2020 00:35:42 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 10:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 10:52:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 26 Feb 2020 10:52:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 10:52:33 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 26 Feb 2020 10:52:33 GMT
ENV JULIA_VERSION=1.3.1
# Wed, 26 Feb 2020 10:53:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='faa707c8343780a6fe5eaf13490355e8190acf8e2c189b9e7ecbddb0fa2643ad' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='965c8fab2214f8ce1b3d449d088561a6de61be42543b48c3bbadaed5b02bf824' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='e028e64f29faa823557819cf4d5887c0b41c28b5225b60f5f2e5e2f38d453458' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='2cef14e892ac317707b39d2afd9ad57a39fb77445ffb7c461a341a4cdf34141a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 26 Feb 2020 10:53:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5cf237473070a9ef7639307699a23bb6c32cd8321bf84c0cf61b6f9c32b44341`  
		Last Modified: Wed, 26 Feb 2020 00:42:02 GMT  
		Size: 23.1 MB (23141399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc0ef46541145d0e75dfc0bcfa47cb6101a8686eb967d3d31c78a1a0bfcf87`  
		Last Modified: Wed, 26 Feb 2020 10:55:37 GMT  
		Size: 7.6 MB (7582721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ccb2d15e1dff9b6dd09834e07e2a2aaca43f66ccfd0db7d7fa72b84deeb6a5`  
		Last Modified: Wed, 26 Feb 2020 10:56:16 GMT  
		Size: 99.3 MB (99277300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
