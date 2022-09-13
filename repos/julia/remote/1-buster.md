## `julia:1-buster`

```console
$ docker pull julia@sha256:757e6f756a4ac7e1dd351370a71f867d2615a0a0b0ac7ee257e6cb405e010d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:ca4898e71d62fb25a953b3150613c30a698045380e044568f769e64ba2ab3d3d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179258675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed204fbfaddc7f01ce514cd79b17c3b4de414b68ee76d72c9268875b3a04e14`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:10:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:10:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:10:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:10:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:10:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dca858d54e664b09949fbcfd89af78473a209bd71139dd756073fe8d36b709`  
		Last Modified: Tue, 13 Sep 2022 06:12:43 GMT  
		Size: 4.5 MB (4468446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c504c7d5a125a875305c933ce2d99158260bf4b1936b7b200dde5d35b44f7125`  
		Last Modified: Tue, 13 Sep 2022 06:13:05 GMT  
		Size: 147.7 MB (147659677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4e4e6805116dbadc17208967d65a633412965fa5affe7acb4893586a720c8c64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171533004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddb39586992606f059c2a24036dabbb1a6932253938cf907aa6530a42a6478d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 04:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 04:28:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 23 Aug 2022 04:28:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 04:28:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 23:01:09 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 23:01:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 12 Sep 2022 23:01:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee5ef9658b8af75e5d8cbd34d5a919e156f9da0588ac3a3b1501cd9b6a98081`  
		Last Modified: Tue, 23 Aug 2022 04:30:31 GMT  
		Size: 4.3 MB (4346922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a5f6b694b9c74a3b0a0ba864354d76030a6f1faf927cd3978816dbb172232c`  
		Last Modified: Mon, 12 Sep 2022 23:03:12 GMT  
		Size: 141.3 MB (141273567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:264d9062a9165467a0c48403da5224735b1a3c1f4077295e5750b24230ca94e0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.9 MB (176852676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab9ad89dc74fe928835d1ec4a545b1eb5988a80d3d6f067a2084bd178c29df2`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Aug 2022 01:03:07 GMT
ADD file:69e3a870d6821a7b0d69402e3d7bc6488f1ed7d86dc5cf7f5f35d5868b72eaf3 in / 
# Tue, 23 Aug 2022 01:03:07 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:52:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:52:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 23 Aug 2022 11:52:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Aug 2022 11:52:24 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:43:52 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:44:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 12 Sep 2022 22:44:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:46d42afa0260ad958104e1c87669868156eb23042a5c897146b1d7009ac682d9`  
		Last Modified: Tue, 23 Aug 2022 01:09:21 GMT  
		Size: 27.8 MB (27797685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564ab79e374248c2778afffda8f2aa8a38a3c6e7d60c75426e41b9773387e20`  
		Last Modified: Tue, 23 Aug 2022 11:54:52 GMT  
		Size: 4.6 MB (4616209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb6ac4337afe1df8235d3b1f9a164964af7ca8dce41d9499bc805d5e47a0180`  
		Last Modified: Mon, 12 Sep 2022 22:45:54 GMT  
		Size: 144.4 MB (144438782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
