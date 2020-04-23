## `julia:1-buster`

```console
$ docker pull julia@sha256:012b434ebf6c3b655b3f2d7fad3e523a724ee404334b48966f13b2844f802ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

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

### `julia:1-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:0f9cd5f28c1d26d7d9cfdfdd40226d00c2e176ab13352d035bfa449dfac73fd1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.6 MB (123609437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af984c969ec31f585a2b2a232c4a701c51175d2f93507a0f99435c8253318ea`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:26 GMT
ADD file:db6122b36f3e70c5f490b50afba99d49fa345f11d0f5c77bb3c6749f8e2a4f81 in / 
# Thu, 23 Apr 2020 01:03:28 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 02:29:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:29:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Apr 2020 02:29:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 02:29:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Apr 2020 02:29:39 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 23 Apr 2020 02:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 23 Apr 2020 02:30:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:50fb0052086928803f00724ca465c89c45dde5b082b1e59dadb8101286dd5ab6`  
		Last Modified: Thu, 23 Apr 2020 01:11:08 GMT  
		Size: 22.7 MB (22705377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227110a4880d38f4743fede6e4730e4c3d14e4d672bf61aee626d3d26a3ff318`  
		Last Modified: Thu, 23 Apr 2020 02:33:10 GMT  
		Size: 3.8 MB (3783610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17207e8313792cf9b0ddc198b39312c059e78ae8bd970704888823ab3959ab7d`  
		Last Modified: Thu, 23 Apr 2020 02:33:44 GMT  
		Size: 97.1 MB (97120450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2de19b37ab7ae978611e90eb00c5180f8d0fb4b8cb508ec0d7651c2e6795b1ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.8 MB (119841746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4094fe1ee31afda478cc5dc4fff7ba720928175707eefc70186f9c1e73e2cbb`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:55 GMT
ADD file:581ee9c3c19f0d971aeda008fd399f59171cae75e8936b967dbf3888db4fc0d0 in / 
# Thu, 23 Apr 2020 00:54:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:43:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:43:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Apr 2020 01:43:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 01:43:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Apr 2020 01:43:17 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 23 Apr 2020 01:43:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 23 Apr 2020 01:43:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bdc84a41f2513e28e99efeff9fcbb196b7df9883fb30532184bd67ca415b4673`  
		Last Modified: Thu, 23 Apr 2020 01:03:27 GMT  
		Size: 25.9 MB (25857800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7cc641b7a762729d84e6590afeeed79d754fd742f6acdbe8f59fdf0c5cc45d`  
		Last Modified: Thu, 23 Apr 2020 01:46:22 GMT  
		Size: 4.3 MB (4315503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c88f5aa79bc6486aae8bf5c53c737508bcb4e0ea795ef2ccbbc4bf53e4a925`  
		Last Modified: Thu, 23 Apr 2020 01:46:46 GMT  
		Size: 89.7 MB (89668443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:c4f18a12e575d503608cb7990991da086c6a7d153683fed06ef15e73599868ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135936679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cde19eddd837bd908dba77a4d1ab4afe9bda9a68935546d408449ab3171aa6`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:36 GMT
ADD file:ca6a74f6b738c738c033152fab2a9aacf22bec5f19a994e6a02b5f919ee33ee9 in / 
# Thu, 23 Apr 2020 00:39:36 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:18:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:18:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 23 Apr 2020 01:18:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 01:18:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 23 Apr 2020 01:18:13 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 23 Apr 2020 01:18:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 23 Apr 2020 01:18:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5d3da8f33b97fc107a05b3255a55836b76df9f817de632b1fb63c6e9c024f0df`  
		Last Modified: Thu, 23 Apr 2020 00:44:35 GMT  
		Size: 27.8 MB (27753972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534650a168845cc2a9e8964f5bbc6bd273be2e1245fead190b85917d1ae36c6e`  
		Last Modified: Thu, 23 Apr 2020 01:20:03 GMT  
		Size: 4.6 MB (4586383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7e4adc01e148769aaa609cbb78bfacbf2a8336746bf39615de9437d64fa636`  
		Last Modified: Thu, 23 Apr 2020 01:20:28 GMT  
		Size: 103.6 MB (103596324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
