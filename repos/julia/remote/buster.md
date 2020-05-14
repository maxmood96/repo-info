## `julia:buster`

```console
$ docker pull julia@sha256:63f4864defd920e5707596c56f3de90462d710bc2a038ee24e02dce4d1545496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:ac1b28281163f8298b018a1d15f329f15a8a8c5e10d2fd4fd13cfc7b8c11785d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138294791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248f01656dfd7ca39159416619408ffc2ac0aa1878f7ebefd3dacfdba30ee7f3`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:44:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:44:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Apr 2020 03:44:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 03:44:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Apr 2020 03:44:37 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 23 Apr 2020 03:45:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 23 Apr 2020 03:45:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350a7ddb9c27e06666be1dc4094983daa7aaec51fec2ed7cdaf71c704e8d78cd`  
		Last Modified: Thu, 23 Apr 2020 03:46:39 GMT  
		Size: 4.4 MB (4436627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8516ad7b1b540b47164fff266ed88dd6ce68f04e1fa9bb2210df74121e33bad2`  
		Last Modified: Thu, 23 Apr 2020 03:47:04 GMT  
		Size: 106.8 MB (106759910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:51af4dae9295f5dfeef412e432e39f1d4a7277c76d66482edd782ed89bb4f185
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123604027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56de8d3a98c3feb7c916be006e3daeb8ee8cdcb57949bc427a6fc0648fc2b7d2`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 13 May 2020 21:14:05 GMT
ADD file:a7ac7c6a5e3ac9b4d748097aae5904495f795062119fc89a4630432982fbc33f in / 
# Wed, 13 May 2020 21:14:08 GMT
CMD ["bash"]
# Thu, 14 May 2020 00:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:46:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 14 May 2020 00:47:00 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 00:47:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 14 May 2020 00:47:01 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 14 May 2020 00:47:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 14 May 2020 00:47:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f88ea38d27a3548118fd61400f9d01d5cb46e9981ea7fd8e552ccc9719bd9750`  
		Last Modified: Wed, 13 May 2020 21:23:35 GMT  
		Size: 22.7 MB (22699937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06580f207e46b2a0266da2b6120fdfbe0b992d914967178faed6616ea61df7f0`  
		Last Modified: Thu, 14 May 2020 00:49:52 GMT  
		Size: 3.8 MB (3783645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648e7a24fb8f8f3e5be7ead8402c0eacf2077e51c998b83ccf7484042f8087f5`  
		Last Modified: Thu, 14 May 2020 00:50:22 GMT  
		Size: 97.1 MB (97120445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6bc0af01de656e9fcbddb3da9bc2d1f3b0fcd52263eaade654f1e2edbbfa8fec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119835589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e9fe2acb38192918ef9afe0cfb99506e0952f30c98030d26fcee2e7833c986`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 13 May 2020 21:43:44 GMT
ADD file:37b141a882e9c33a09f7554ab39e3ba9c7f2b12e916c721436bd85817951eb4c in / 
# Wed, 13 May 2020 21:43:47 GMT
CMD ["bash"]
# Thu, 14 May 2020 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 01:44:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 14 May 2020 01:44:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 01:44:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 14 May 2020 01:44:24 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 14 May 2020 01:44:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 14 May 2020 01:44:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b24dc5b5f4f0ffe0f8a33241aa35f3d74ee4213bc2b87eb3ec4b72a6e70ba7bc`  
		Last Modified: Wed, 13 May 2020 21:53:15 GMT  
		Size: 25.9 MB (25851785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692fbf20cba3828d87c4087ab47220ae21360df799b3f065741c4fa8c58c01b0`  
		Last Modified: Thu, 14 May 2020 01:46:41 GMT  
		Size: 4.3 MB (4315465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac55ec88dd65ca7b1eefb8c34011df2793f96606bc13734dda18ae4b60de418`  
		Last Modified: Thu, 14 May 2020 01:47:07 GMT  
		Size: 89.7 MB (89668339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:101f33a293de62011760ca397039a61a93d54857ef2f6381361a29dab8807efa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135930541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745222f02a147d8b61702661278dec6eed7fe878c45b6de818c9b419c2ea312c`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 13 May 2020 21:39:26 GMT
ADD file:e92e4e13785400e1d0cbdfd2b1d0454f6e9b4e5db46a134c637427c1d521f5c5 in / 
# Wed, 13 May 2020 21:39:26 GMT
CMD ["bash"]
# Thu, 14 May 2020 00:24:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 00:24:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 14 May 2020 00:24:11 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 00:24:11 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 14 May 2020 00:24:11 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 14 May 2020 00:24:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 14 May 2020 00:24:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:719e323d8af1942809d715e86b7671949520675686dd460851d76bf569d8a8e8`  
		Last Modified: Wed, 13 May 2020 21:46:32 GMT  
		Size: 27.7 MB (27747747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb08299781dd5a3148d06a87085d8b7a7829c03e6d19fb0e2c01a8a21693e2e`  
		Last Modified: Thu, 14 May 2020 00:26:24 GMT  
		Size: 4.6 MB (4586315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc0dd4d4708b6c808876194f121d1271ca5593cd9d0ffce376171a0c2d21604`  
		Last Modified: Thu, 14 May 2020 00:27:02 GMT  
		Size: 103.6 MB (103596479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
