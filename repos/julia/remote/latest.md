## `julia:latest`

```console
$ docker pull julia@sha256:da222197985f14e55abe4df8b56705fd1dca0a1df8d50b2c7667eed48b8266cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:b9edd30e812f52d3c347a2739440ab12b5e02aadebcf49db338dc0fd2a8230ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138288579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdf9475683023b7b3751a67557010495c39d92b2ec4078ff4c9ff2a0bba1494`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 13 May 2020 21:20:38 GMT
ADD file:ca8f84daab6688a5d8efa1fc57c754c162584fc99cd98a8ea357065661d6a48b in / 
# Wed, 13 May 2020 21:20:38 GMT
CMD ["bash"]
# Thu, 14 May 2020 03:23:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:23:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 14 May 2020 03:23:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 03:23:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 14 May 2020 03:23:10 GMT
ENV JULIA_VERSION=1.4.1
# Thu, 14 May 2020 03:23:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='fd6d8cadaed678174c3caefb92207a3b0e8da9f926af6703fb4d1e4e4f50610a' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='bdcf24e0365f16092838daf7059bf5c0036bff9dc418511010e79249d9f71e96' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='788dc1e79344b52f65358ce4406dc5304bafd82c6af50bfa92a6ee5ea998e678' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='765e614b2754b20d50bae475dd9f3b794f445915084afa42523fd1b14e4c91fe' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 14 May 2020 03:23:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5b54d594fba7f30e90c967a80607905ba8d90ca8be45d5a4d30e69d75e65430b`  
		Last Modified: Wed, 13 May 2020 21:26:23 GMT  
		Size: 27.1 MB (27091990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced8ffeab739558204f90f9d01acb6e34564f6d96f3f8324351344e5f8d0f94d`  
		Last Modified: Thu, 14 May 2020 03:24:51 GMT  
		Size: 4.4 MB (4436646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3aa9151f9dcf9b6b294c4352325cf93d46b3d43b1a2781a4a1fc0dccd0e0491`  
		Last Modified: Thu, 14 May 2020 03:25:13 GMT  
		Size: 106.8 MB (106759943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm variant v7

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

### `julia:latest` - linux; arm64 variant v8

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

### `julia:latest` - linux; 386

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

### `julia:latest` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:ce1344a958575bf7e93027fd1e91daf1ec82d14ffca51db3137142daaf833428
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870430922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14d4005a6b6069d766cf41d2745eae1f4e6431fac6a5e3864c0c140f046f6ff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:32:34 GMT
ENV JULIA_VERSION=1.4.1
# Wed, 13 May 2020 14:32:35 GMT
ENV JULIA_SHA256=953090cf2a3690791df7550175a8969e8de15cbd84d815975b6495cc884deab6
# Wed, 13 May 2020 14:35:35 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:35:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be990d0e5ebe83a00402289d3ebba78a3187016ea43091bd7ffca2d63ef72fc`  
		Last Modified: Wed, 13 May 2020 14:43:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25db2c2382c5c54fac4ec3e1493033b3afe09b8d9a013aa1c98d7c02da812568`  
		Last Modified: Wed, 13 May 2020 14:43:54 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c848a9e5fda52e23f13a7b09d7a656e9937fb2cd6313be8ffeb1104471820b`  
		Last Modified: Wed, 13 May 2020 14:44:27 GMT  
		Size: 138.5 MB (138536449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4ac3b156eff387f68d1e7cb6fe7d15b1c99f1cdf82cac5e6542e794d1e378d`  
		Last Modified: Wed, 13 May 2020 14:43:54 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:d5b0ca5c6b773f1806b0dbf636e7d31f1a4da71b980020c59ae591cd92652849
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847332331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437f96d94ad9d4d18d4c031e4ab8f1cca7269dd4c818bb7f34548a50edc6b453`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:35:46 GMT
ENV JULIA_VERSION=1.4.1
# Wed, 13 May 2020 14:35:47 GMT
ENV JULIA_SHA256=953090cf2a3690791df7550175a8969e8de15cbd84d815975b6495cc884deab6
# Wed, 13 May 2020 14:37:53 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:37:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40bbcd70e265bc989721235da0fbad8cdebe77542fa25464d8f6672cd07c2af`  
		Last Modified: Wed, 13 May 2020 14:44:42 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b23c46bdcb951889977990b5cb9bdcd16e5e5641a1fc7a6f9747e9f048f1e3`  
		Last Modified: Wed, 13 May 2020 14:44:43 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd25c005aa5fac6239a49b1f181568ef8c8151ee124ffba640a4fb7710b0c753`  
		Last Modified: Wed, 13 May 2020 14:47:09 GMT  
		Size: 129.0 MB (128994906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da14290dc98c06f5f7ae0815807cd721414e0131d2d469600613840ad530985d`  
		Last Modified: Wed, 13 May 2020 14:44:42 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
