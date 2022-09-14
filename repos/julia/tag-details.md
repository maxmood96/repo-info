<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-alpine`](#julia1-alpine)
-	[`julia:1-alpine3.15`](#julia1-alpine315)
-	[`julia:1-alpine3.16`](#julia1-alpine316)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-buster`](#julia1-buster)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.6`](#julia16)
-	[`julia:1.6-alpine`](#julia16-alpine)
-	[`julia:1.6-alpine3.15`](#julia16-alpine315)
-	[`julia:1.6-alpine3.16`](#julia16-alpine316)
-	[`julia:1.6-bullseye`](#julia16-bullseye)
-	[`julia:1.6-buster`](#julia16-buster)
-	[`julia:1.6-windowsservercore`](#julia16-windowsservercore)
-	[`julia:1.6-windowsservercore-1809`](#julia16-windowsservercore-1809)
-	[`julia:1.6-windowsservercore-ltsc2022`](#julia16-windowsservercore-ltsc2022)
-	[`julia:1.6.7`](#julia167)
-	[`julia:1.6.7-alpine`](#julia167-alpine)
-	[`julia:1.6.7-alpine3.15`](#julia167-alpine315)
-	[`julia:1.6.7-alpine3.16`](#julia167-alpine316)
-	[`julia:1.6.7-bullseye`](#julia167-bullseye)
-	[`julia:1.6.7-buster`](#julia167-buster)
-	[`julia:1.6.7-windowsservercore`](#julia167-windowsservercore)
-	[`julia:1.6.7-windowsservercore-1809`](#julia167-windowsservercore-1809)
-	[`julia:1.6.7-windowsservercore-ltsc2022`](#julia167-windowsservercore-ltsc2022)
-	[`julia:1.8`](#julia18)
-	[`julia:1.8-alpine`](#julia18-alpine)
-	[`julia:1.8-alpine3.15`](#julia18-alpine315)
-	[`julia:1.8-alpine3.16`](#julia18-alpine316)
-	[`julia:1.8-bullseye`](#julia18-bullseye)
-	[`julia:1.8-buster`](#julia18-buster)
-	[`julia:1.8-windowsservercore`](#julia18-windowsservercore)
-	[`julia:1.8-windowsservercore-1809`](#julia18-windowsservercore-1809)
-	[`julia:1.8-windowsservercore-ltsc2022`](#julia18-windowsservercore-ltsc2022)
-	[`julia:1.8.1`](#julia181)
-	[`julia:1.8.1-alpine`](#julia181-alpine)
-	[`julia:1.8.1-alpine3.15`](#julia181-alpine315)
-	[`julia:1.8.1-alpine3.16`](#julia181-alpine316)
-	[`julia:1.8.1-bullseye`](#julia181-bullseye)
-	[`julia:1.8.1-buster`](#julia181-buster)
-	[`julia:1.8.1-windowsservercore`](#julia181-windowsservercore)
-	[`julia:1.8.1-windowsservercore-1809`](#julia181-windowsservercore-1809)
-	[`julia:1.8.1-windowsservercore-ltsc2022`](#julia181-windowsservercore-ltsc2022)
-	[`julia:alpine`](#juliaalpine)
-	[`julia:alpine3.15`](#juliaalpine315)
-	[`julia:alpine3.16`](#juliaalpine316)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:buster`](#juliabuster)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:937a26e034923edfc3c8a2dc5f0d5028e0f388b0790e7bc02de53c39d064fcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine3.15`

```console
$ docker pull julia@sha256:5a115d135d595fdb6f5cdba845f72eee906dd707e48de61eac72157ac2bf9941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:ff319b672dcbfd21237bb530ba7492aa01c9178a5218917d1b89170c7cfaa5ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c1754b206335a99b344bcc53aacfbb467c4b47f9ad4924de72226e29c04025`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:31:25 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0dfb1f33ed58261036c68d7560d680df65801f4b059a05fe06e948193369c`  
		Last Modified: Mon, 12 Sep 2022 22:34:49 GMT  
		Size: 149.3 MB (149258181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine3.16`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:a6f06b8560c41b9bdf6b177f2a2dfe8d25a5bb7f026e7bc7f9e7d7c810bbd543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-buster`

```console
$ docker pull julia@sha256:69fb0c560054f6a7b4188b0bfde186950f4904eb6bfad43546e5391ca9cfd6bb
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
$ docker pull julia@sha256:057b284350db760bc44819f2909cb2f8a95a9a694390e5e01871d6e36c11d78d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171524573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d93b15ca1982cbcc1b02ab350119160e5af7041bd09f3bdcb22da8adbdc841d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:54:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa187f35c48ac07504837d6c194722424c0c81baca5ed508a23d828efc9666`  
		Last Modified: Tue, 13 Sep 2022 06:56:16 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc66ab2dccb76145b27255e0261d2f25bce448781874c0a7cf876fe84f79f7`  
		Last Modified: Tue, 13 Sep 2022 06:56:37 GMT  
		Size: 141.3 MB (141273540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:2240953ec1fef6783d4117f4a75f16ac5a59b22323cffc5b39c56d92128f5aaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176846643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0fb2fa1e54f4a3754ecb337c1477c3d30067cecad272941d154393d52f7981`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:00 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:46:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a7b851a490ad11fdc5f9b5349c6e0938d538849e48fa0d16bcf71d7cd7b112`  
		Last Modified: Tue, 13 Sep 2022 13:48:27 GMT  
		Size: 4.6 MB (4616868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f253c99ab3897bca0e37018c75ff6189c2bac9d9489b35d6f05b2e04a3b28`  
		Last Modified: Tue, 13 Sep 2022 13:48:45 GMT  
		Size: 144.4 MB (144438823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:4e88e4f8e75b83804369da22e073a4b4ee182786184554f0f7fe4bdac80a4a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:f21df5147ee24f953f369cca1661278da236866aeb2351a84d5afcbe0dc47a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:12dfddf543c66c842e918b5c92bdb2da960d977556a2a4f65c9a6476a1146543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6`

```console
$ docker pull julia@sha256:a85378ca4fea1c4e3ca29bc350b276105e1ac7ea9b38dcd2d94e132cf4726108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.6` - linux; amd64

```console
$ docker pull julia@sha256:a92fa49638e95c8adc3b46668d12f40e2529d215f7f8749d10dd98eb6f2c37cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156470613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23fc350f55bcb59273cf973c88a94833248346176c7f56db2a64493ee6bda66`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:10:47 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:11:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:11:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0c496e9325a15d72702260db28989bc2eec1a99b79d36c84705c96d01301b`  
		Last Modified: Tue, 13 Sep 2022 06:13:45 GMT  
		Size: 122.6 MB (122639920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; arm variant v7

```console
$ docker pull julia@sha256:5c235892f52110d533f86b531306bc915ce878cbbdf02dc56f4bc505e9b0048e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142483774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0287779f83fcca690f30e50b590ec8d9fc52181a9c9babf77741b7447ea88`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:41:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 11:41:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 11:42:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 11:42:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6da6a3f5a0909f40f0c87c61324ae06644717d53d6be65f6cd31d181f8a5cb`  
		Last Modified: Tue, 13 Sep 2022 11:43:06 GMT  
		Size: 2.2 MB (2228909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f4e71155bdd16e8b8ccde63ee06e358c0e34aa3fae938619e4ad350545196`  
		Last Modified: Tue, 13 Sep 2022 11:43:28 GMT  
		Size: 113.7 MB (113687806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:edca1e20e1fca88b5d7898ba5dc49e6e12222cdf19a68321023ded2a417353f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148681181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd73aa7333c6afdc919b97262257604b90bb317212ac04ec74a321826b32e5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:54:21 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:54:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2fd325a99ad06611e5a0080c68406ed9f9abba1bfd201fd7827015d43a877d`  
		Last Modified: Tue, 13 Sep 2022 06:57:11 GMT  
		Size: 116.2 MB (116213253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; 386

```console
$ docker pull julia@sha256:3941406f037a31871f1858c482f6edd1e88566d768e5c74388ec6880201abeb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155006258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabf23bb28ed53c08c014f52b8e26cb2b8bd1f4725e714ae70eb58a803460f5f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:27 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 13:46:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1035982cb12085f93011f759a3b62cd50bc754b3e2c19bcd2aea8fac39cc946f`  
		Last Modified: Tue, 13 Sep 2022 13:49:17 GMT  
		Size: 120.1 MB (120090725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:644d19dcbfeafc426b55272d39aa9de0a726a26c787d76270a23a08975b8d906
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481594345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dd32d24916b20290b6bc6cac228d0494dca501603deb9e1800a4253582675f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:07:52 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:07:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:07:54 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:09:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c831f7593aee39d97551da204a861e05736dbc407f90afbc51129299ab39fb`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40644ea92254d602fe561f9820092bad40a2722661b9b9b1f198541b6b000ef5`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b42cf56bd8df7dc68e75819f671aac911872030a9878e313490278167ea4be6`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e55fdd6d2d2e7e18bc8ed2382d05ed462b678138437dbdfe16935fb1fd7aec`  
		Last Modified: Wed, 14 Sep 2022 15:37:20 GMT  
		Size: 134.6 MB (134637716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f9acec052a78ace03b0e9ff2822fa65a0c4d9bbbb20eb1dd76f82067d6a9`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:9f44d8acd087d17ab68d94cb6e05e7c4c68bf1c780c27500e5c3ea8b089b14ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e8cfeb87030fc9b54cedf3bbbf7cbee2d7b25b34d4e7fed60283bca7708b0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:09:35 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:09:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:09:37 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2220a85f440093d8ffc3dfceb27ffaa979230817172e729f0a4a89afc853d6`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1104e8b885c925dc4781d123b39f654d0c1681cd11a7a74017d396d798a9`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2790b7f1736a1ebb05e257efa31fe620c36a9ba22a3a094665ec328548fb45c`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfbe02615e95687de43ac0d5879b3b73bb23e3f8b108981a5141ac59f10a45`  
		Last Modified: Wed, 14 Sep 2022 15:37:59 GMT  
		Size: 134.4 MB (134422685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf99bd27c5c88bcb1c104ac4c6f9ac42c91645dba1962fcf29269f6da9b54e`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine`

```console
$ docker pull julia@sha256:abad5660f5a25b83328226f94c06f079ae52e1516c0964ca60425f8609470e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine` - linux; amd64

```console
$ docker pull julia@sha256:d3ce5d6d5d6f52656a02cf4c856bebd70b3bcbc03dcbe998dd8742fe6bc69a33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf39300b6c77f62601cb1d00732814d855bb6adb601fcfaa30ee52fc91e391e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Aug 2022 20:44:03 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 09 Aug 2022 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 09 Aug 2022 20:44:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330082d37d521e85ed048135a49bb04735375b78ee4f62596d0fe91ddf609bd`  
		Last Modified: Tue, 09 Aug 2022 20:48:32 GMT  
		Size: 121.8 MB (121828643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine3.15`

```console
$ docker pull julia@sha256:3eaf1cf9731fbedfca9fc5ab8120a5f8168fd29ce23767061f64a02f6fb38091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:bbbffe7594e3fbb20aedd6c3ba81e9d5d327cd9f63728c7dbe809260d53d2ace
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124652106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b946aaf71e28d5eb07e343a7c2cee7b04d8ac744c4f1d362d64fd0e369931842`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Aug 2022 20:44:22 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 09 Aug 2022 20:44:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 09 Aug 2022 20:44:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8ddc086b261016ce741f48368107159bdc66980c1f74a6324a65fc523cacb9`  
		Last Modified: Tue, 09 Aug 2022 20:49:06 GMT  
		Size: 121.8 MB (121828594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine3.16`

```console
$ docker pull julia@sha256:abad5660f5a25b83328226f94c06f079ae52e1516c0964ca60425f8609470e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:d3ce5d6d5d6f52656a02cf4c856bebd70b3bcbc03dcbe998dd8742fe6bc69a33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf39300b6c77f62601cb1d00732814d855bb6adb601fcfaa30ee52fc91e391e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Aug 2022 20:44:03 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 09 Aug 2022 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 09 Aug 2022 20:44:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330082d37d521e85ed048135a49bb04735375b78ee4f62596d0fe91ddf609bd`  
		Last Modified: Tue, 09 Aug 2022 20:48:32 GMT  
		Size: 121.8 MB (121828643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-bullseye`

```console
$ docker pull julia@sha256:9b19e73aa393f66ab0da50ca02854d5d6d46ec7c61c3ad84b6f512ef2b2c43a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a92fa49638e95c8adc3b46668d12f40e2529d215f7f8749d10dd98eb6f2c37cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156470613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23fc350f55bcb59273cf973c88a94833248346176c7f56db2a64493ee6bda66`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:10:47 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:11:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:11:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0c496e9325a15d72702260db28989bc2eec1a99b79d36c84705c96d01301b`  
		Last Modified: Tue, 13 Sep 2022 06:13:45 GMT  
		Size: 122.6 MB (122639920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:5c235892f52110d533f86b531306bc915ce878cbbdf02dc56f4bc505e9b0048e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142483774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0287779f83fcca690f30e50b590ec8d9fc52181a9c9babf77741b7447ea88`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:41:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 11:41:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 11:42:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 11:42:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6da6a3f5a0909f40f0c87c61324ae06644717d53d6be65f6cd31d181f8a5cb`  
		Last Modified: Tue, 13 Sep 2022 11:43:06 GMT  
		Size: 2.2 MB (2228909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f4e71155bdd16e8b8ccde63ee06e358c0e34aa3fae938619e4ad350545196`  
		Last Modified: Tue, 13 Sep 2022 11:43:28 GMT  
		Size: 113.7 MB (113687806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:edca1e20e1fca88b5d7898ba5dc49e6e12222cdf19a68321023ded2a417353f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148681181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd73aa7333c6afdc919b97262257604b90bb317212ac04ec74a321826b32e5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:54:21 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:54:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2fd325a99ad06611e5a0080c68406ed9f9abba1bfd201fd7827015d43a877d`  
		Last Modified: Tue, 13 Sep 2022 06:57:11 GMT  
		Size: 116.2 MB (116213253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3941406f037a31871f1858c482f6edd1e88566d768e5c74388ec6880201abeb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155006258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabf23bb28ed53c08c014f52b8e26cb2b8bd1f4725e714ae70eb58a803460f5f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:27 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 13:46:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1035982cb12085f93011f759a3b62cd50bc754b3e2c19bcd2aea8fac39cc946f`  
		Last Modified: Tue, 13 Sep 2022 13:49:17 GMT  
		Size: 120.1 MB (120090725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-buster`

```console
$ docker pull julia@sha256:11a9403ba099b1a7c34cd6a657c50c0fbf92e7f478afe95e34746e3b3b92de00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6-buster` - linux; amd64

```console
$ docker pull julia@sha256:487064e9ad24d34877e0e2048a33f74646d38a5f9cf8fdadba30fdcdcced7e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154248703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b36fd9468d7d0e8a41bda44216d86d2ad7f03c3880c03c1296ad218fc15a42`
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
# Tue, 13 Sep 2022 06:11:07 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:11:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:11:22 GMT
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
	-	`sha256:99d42bcee1a8f29c6454067102ab79ef975bb5ce9e54677dcad8c23830d7b446`  
		Last Modified: Tue, 13 Sep 2022 06:14:15 GMT  
		Size: 122.6 MB (122649705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:983207dad9750fcd6194de9e3004a33f9b01849797d98ff6613b484c1914758b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140247878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56459e18d40e1d1770f76be018b9c466783bd627c4ccc1196751235696c77f8`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 03:43:14 GMT
ADD file:0a80cba5196c5f463d85aeb456ee0f5778155ac5b1d3ce93a2023f1141aac44a in / 
# Tue, 13 Sep 2022 03:43:14 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:42:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 11:42:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:42:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 11:42:18 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 11:42:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 11:42:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:04df89f99dde583959eeb3f2964381f6e5a3199fa335ea1b9862aab596638515`  
		Last Modified: Tue, 13 Sep 2022 03:50:50 GMT  
		Size: 22.7 MB (22740495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cd1df414e2cf557c09628189f6ec181fdae28a2f877040cc559890386a8eb`  
		Last Modified: Tue, 13 Sep 2022 11:43:41 GMT  
		Size: 3.8 MB (3811599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7168a35099c49997bc5a49c1ac3a8082b5ff384fb82391e9ed52921f978e3291`  
		Last Modified: Tue, 13 Sep 2022 11:44:04 GMT  
		Size: 113.7 MB (113695784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:56356e3b66a3e1fa183a329bab2ed7a38b2dfe3f4a3d8bf944dea753875c4eb1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146473259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f4e5e0ff633767d739da3ee78b599d3af08a47c338f956d64843f83439ee86`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:54:47 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:55:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:55:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa187f35c48ac07504837d6c194722424c0c81baca5ed508a23d828efc9666`  
		Last Modified: Tue, 13 Sep 2022 06:56:16 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783963f8e1ea399bbc9bcaf86fd898dd341c177cd3cf525beb83d6e4a91f469`  
		Last Modified: Tue, 13 Sep 2022 06:57:39 GMT  
		Size: 116.2 MB (116222226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; 386

```console
$ docker pull julia@sha256:974048b38530ab17ae42bad4d5daf40fff0dea006dfe0468d5af708fb5d265c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152511131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad37e35f5549af6c074a618052865f7055ac457d0d73c2ad01c12707d8a165`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:54 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 13:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:47:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a7b851a490ad11fdc5f9b5349c6e0938d538849e48fa0d16bcf71d7cd7b112`  
		Last Modified: Tue, 13 Sep 2022 13:48:27 GMT  
		Size: 4.6 MB (4616868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a608952f9b2635d6aa75c873099a6ca801fa330d9f5fff5dc0fa226eda98ca8`  
		Last Modified: Tue, 13 Sep 2022 13:49:44 GMT  
		Size: 120.1 MB (120103311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore`

```console
$ docker pull julia@sha256:4279aeb45596ea0abc3f53e4671560ec05f127b506ac2cf3f793862982c9523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.6-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:644d19dcbfeafc426b55272d39aa9de0a726a26c787d76270a23a08975b8d906
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481594345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dd32d24916b20290b6bc6cac228d0494dca501603deb9e1800a4253582675f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:07:52 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:07:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:07:54 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:09:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c831f7593aee39d97551da204a861e05736dbc407f90afbc51129299ab39fb`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40644ea92254d602fe561f9820092bad40a2722661b9b9b1f198541b6b000ef5`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b42cf56bd8df7dc68e75819f671aac911872030a9878e313490278167ea4be6`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e55fdd6d2d2e7e18bc8ed2382d05ed462b678138437dbdfe16935fb1fd7aec`  
		Last Modified: Wed, 14 Sep 2022 15:37:20 GMT  
		Size: 134.6 MB (134637716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f9acec052a78ace03b0e9ff2822fa65a0c4d9bbbb20eb1dd76f82067d6a9`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:9f44d8acd087d17ab68d94cb6e05e7c4c68bf1c780c27500e5c3ea8b089b14ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e8cfeb87030fc9b54cedf3bbbf7cbee2d7b25b34d4e7fed60283bca7708b0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:09:35 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:09:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:09:37 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2220a85f440093d8ffc3dfceb27ffaa979230817172e729f0a4a89afc853d6`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1104e8b885c925dc4781d123b39f654d0c1681cd11a7a74017d396d798a9`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2790b7f1736a1ebb05e257efa31fe620c36a9ba22a3a094665ec328548fb45c`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfbe02615e95687de43ac0d5879b3b73bb23e3f8b108981a5141ac59f10a45`  
		Last Modified: Wed, 14 Sep 2022 15:37:59 GMT  
		Size: 134.4 MB (134422685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf99bd27c5c88bcb1c104ac4c6f9ac42c91645dba1962fcf29269f6da9b54e`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:b2e64d8c3e5ff5ebf70f50bd8c810dcff14af28dea451ec074545a5f96004a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:1.6-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:9f44d8acd087d17ab68d94cb6e05e7c4c68bf1c780c27500e5c3ea8b089b14ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e8cfeb87030fc9b54cedf3bbbf7cbee2d7b25b34d4e7fed60283bca7708b0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:09:35 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:09:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:09:37 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2220a85f440093d8ffc3dfceb27ffaa979230817172e729f0a4a89afc853d6`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1104e8b885c925dc4781d123b39f654d0c1681cd11a7a74017d396d798a9`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2790b7f1736a1ebb05e257efa31fe620c36a9ba22a3a094665ec328548fb45c`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfbe02615e95687de43ac0d5879b3b73bb23e3f8b108981a5141ac59f10a45`  
		Last Modified: Wed, 14 Sep 2022 15:37:59 GMT  
		Size: 134.4 MB (134422685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf99bd27c5c88bcb1c104ac4c6f9ac42c91645dba1962fcf29269f6da9b54e`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:3acb97bc3707ad228c98b5ada87f6db6c75ca870226a7e2ca34fb2e346073e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:1.6-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:644d19dcbfeafc426b55272d39aa9de0a726a26c787d76270a23a08975b8d906
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481594345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dd32d24916b20290b6bc6cac228d0494dca501603deb9e1800a4253582675f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:07:52 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:07:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:07:54 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:09:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c831f7593aee39d97551da204a861e05736dbc407f90afbc51129299ab39fb`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40644ea92254d602fe561f9820092bad40a2722661b9b9b1f198541b6b000ef5`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b42cf56bd8df7dc68e75819f671aac911872030a9878e313490278167ea4be6`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e55fdd6d2d2e7e18bc8ed2382d05ed462b678138437dbdfe16935fb1fd7aec`  
		Last Modified: Wed, 14 Sep 2022 15:37:20 GMT  
		Size: 134.6 MB (134637716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f9acec052a78ace03b0e9ff2822fa65a0c4d9bbbb20eb1dd76f82067d6a9`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7`

```console
$ docker pull julia@sha256:a85378ca4fea1c4e3ca29bc350b276105e1ac7ea9b38dcd2d94e132cf4726108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.6.7` - linux; amd64

```console
$ docker pull julia@sha256:a92fa49638e95c8adc3b46668d12f40e2529d215f7f8749d10dd98eb6f2c37cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156470613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23fc350f55bcb59273cf973c88a94833248346176c7f56db2a64493ee6bda66`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:10:47 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:11:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:11:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0c496e9325a15d72702260db28989bc2eec1a99b79d36c84705c96d01301b`  
		Last Modified: Tue, 13 Sep 2022 06:13:45 GMT  
		Size: 122.6 MB (122639920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - linux; arm variant v7

```console
$ docker pull julia@sha256:5c235892f52110d533f86b531306bc915ce878cbbdf02dc56f4bc505e9b0048e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142483774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0287779f83fcca690f30e50b590ec8d9fc52181a9c9babf77741b7447ea88`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:41:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 11:41:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 11:42:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 11:42:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6da6a3f5a0909f40f0c87c61324ae06644717d53d6be65f6cd31d181f8a5cb`  
		Last Modified: Tue, 13 Sep 2022 11:43:06 GMT  
		Size: 2.2 MB (2228909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f4e71155bdd16e8b8ccde63ee06e358c0e34aa3fae938619e4ad350545196`  
		Last Modified: Tue, 13 Sep 2022 11:43:28 GMT  
		Size: 113.7 MB (113687806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:edca1e20e1fca88b5d7898ba5dc49e6e12222cdf19a68321023ded2a417353f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148681181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd73aa7333c6afdc919b97262257604b90bb317212ac04ec74a321826b32e5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:54:21 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:54:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2fd325a99ad06611e5a0080c68406ed9f9abba1bfd201fd7827015d43a877d`  
		Last Modified: Tue, 13 Sep 2022 06:57:11 GMT  
		Size: 116.2 MB (116213253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - linux; 386

```console
$ docker pull julia@sha256:3941406f037a31871f1858c482f6edd1e88566d768e5c74388ec6880201abeb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155006258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabf23bb28ed53c08c014f52b8e26cb2b8bd1f4725e714ae70eb58a803460f5f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:27 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 13:46:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1035982cb12085f93011f759a3b62cd50bc754b3e2c19bcd2aea8fac39cc946f`  
		Last Modified: Tue, 13 Sep 2022 13:49:17 GMT  
		Size: 120.1 MB (120090725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:644d19dcbfeafc426b55272d39aa9de0a726a26c787d76270a23a08975b8d906
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481594345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dd32d24916b20290b6bc6cac228d0494dca501603deb9e1800a4253582675f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:07:52 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:07:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:07:54 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:09:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c831f7593aee39d97551da204a861e05736dbc407f90afbc51129299ab39fb`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40644ea92254d602fe561f9820092bad40a2722661b9b9b1f198541b6b000ef5`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b42cf56bd8df7dc68e75819f671aac911872030a9878e313490278167ea4be6`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e55fdd6d2d2e7e18bc8ed2382d05ed462b678138437dbdfe16935fb1fd7aec`  
		Last Modified: Wed, 14 Sep 2022 15:37:20 GMT  
		Size: 134.6 MB (134637716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f9acec052a78ace03b0e9ff2822fa65a0c4d9bbbb20eb1dd76f82067d6a9`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:9f44d8acd087d17ab68d94cb6e05e7c4c68bf1c780c27500e5c3ea8b089b14ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e8cfeb87030fc9b54cedf3bbbf7cbee2d7b25b34d4e7fed60283bca7708b0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:09:35 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:09:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:09:37 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2220a85f440093d8ffc3dfceb27ffaa979230817172e729f0a4a89afc853d6`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1104e8b885c925dc4781d123b39f654d0c1681cd11a7a74017d396d798a9`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2790b7f1736a1ebb05e257efa31fe620c36a9ba22a3a094665ec328548fb45c`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfbe02615e95687de43ac0d5879b3b73bb23e3f8b108981a5141ac59f10a45`  
		Last Modified: Wed, 14 Sep 2022 15:37:59 GMT  
		Size: 134.4 MB (134422685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf99bd27c5c88bcb1c104ac4c6f9ac42c91645dba1962fcf29269f6da9b54e`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine`

```console
$ docker pull julia@sha256:abad5660f5a25b83328226f94c06f079ae52e1516c0964ca60425f8609470e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.7-alpine` - linux; amd64

```console
$ docker pull julia@sha256:d3ce5d6d5d6f52656a02cf4c856bebd70b3bcbc03dcbe998dd8742fe6bc69a33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf39300b6c77f62601cb1d00732814d855bb6adb601fcfaa30ee52fc91e391e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Aug 2022 20:44:03 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 09 Aug 2022 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 09 Aug 2022 20:44:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330082d37d521e85ed048135a49bb04735375b78ee4f62596d0fe91ddf609bd`  
		Last Modified: Tue, 09 Aug 2022 20:48:32 GMT  
		Size: 121.8 MB (121828643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine3.15`

```console
$ docker pull julia@sha256:3eaf1cf9731fbedfca9fc5ab8120a5f8168fd29ce23767061f64a02f6fb38091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.7-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:bbbffe7594e3fbb20aedd6c3ba81e9d5d327cd9f63728c7dbe809260d53d2ace
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124652106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b946aaf71e28d5eb07e343a7c2cee7b04d8ac744c4f1d362d64fd0e369931842`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Aug 2022 20:44:22 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 09 Aug 2022 20:44:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 09 Aug 2022 20:44:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8ddc086b261016ce741f48368107159bdc66980c1f74a6324a65fc523cacb9`  
		Last Modified: Tue, 09 Aug 2022 20:49:06 GMT  
		Size: 121.8 MB (121828594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine3.16`

```console
$ docker pull julia@sha256:abad5660f5a25b83328226f94c06f079ae52e1516c0964ca60425f8609470e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.7-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:d3ce5d6d5d6f52656a02cf4c856bebd70b3bcbc03dcbe998dd8742fe6bc69a33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf39300b6c77f62601cb1d00732814d855bb6adb601fcfaa30ee52fc91e391e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Aug 2022 20:44:03 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 09 Aug 2022 20:44:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 09 Aug 2022 20:44:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f330082d37d521e85ed048135a49bb04735375b78ee4f62596d0fe91ddf609bd`  
		Last Modified: Tue, 09 Aug 2022 20:48:32 GMT  
		Size: 121.8 MB (121828643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-bullseye`

```console
$ docker pull julia@sha256:9b19e73aa393f66ab0da50ca02854d5d6d46ec7c61c3ad84b6f512ef2b2c43a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:a92fa49638e95c8adc3b46668d12f40e2529d215f7f8749d10dd98eb6f2c37cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156470613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23fc350f55bcb59273cf973c88a94833248346176c7f56db2a64493ee6bda66`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:10:47 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:11:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:11:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa0c496e9325a15d72702260db28989bc2eec1a99b79d36c84705c96d01301b`  
		Last Modified: Tue, 13 Sep 2022 06:13:45 GMT  
		Size: 122.6 MB (122639920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:5c235892f52110d533f86b531306bc915ce878cbbdf02dc56f4bc505e9b0048e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142483774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b0287779f83fcca690f30e50b590ec8d9fc52181a9c9babf77741b7447ea88`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 03:42:37 GMT
ADD file:04b0c48a2d326e2ac4255df4a6165508f0d29d8a32147fb8df6bf9504b8f6b09 in / 
# Tue, 13 Sep 2022 03:42:37 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:41:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 11:41:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 11:41:38 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 11:42:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 11:42:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:43caeee1782255456dd3403ae8e6ba191802c3deb004ca68ce0420b30368995d`  
		Last Modified: Tue, 13 Sep 2022 03:49:46 GMT  
		Size: 26.6 MB (26567059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6da6a3f5a0909f40f0c87c61324ae06644717d53d6be65f6cd31d181f8a5cb`  
		Last Modified: Tue, 13 Sep 2022 11:43:06 GMT  
		Size: 2.2 MB (2228909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f4e71155bdd16e8b8ccde63ee06e358c0e34aa3fae938619e4ad350545196`  
		Last Modified: Tue, 13 Sep 2022 11:43:28 GMT  
		Size: 113.7 MB (113687806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:edca1e20e1fca88b5d7898ba5dc49e6e12222cdf19a68321023ded2a417353f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148681181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fd73aa7333c6afdc919b97262257604b90bb317212ac04ec74a321826b32e5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:54:21 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:54:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2fd325a99ad06611e5a0080c68406ed9f9abba1bfd201fd7827015d43a877d`  
		Last Modified: Tue, 13 Sep 2022 06:57:11 GMT  
		Size: 116.2 MB (116213253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:3941406f037a31871f1858c482f6edd1e88566d768e5c74388ec6880201abeb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155006258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabf23bb28ed53c08c014f52b8e26cb2b8bd1f4725e714ae70eb58a803460f5f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:27 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 13:46:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1035982cb12085f93011f759a3b62cd50bc754b3e2c19bcd2aea8fac39cc946f`  
		Last Modified: Tue, 13 Sep 2022 13:49:17 GMT  
		Size: 120.1 MB (120090725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-buster`

```console
$ docker pull julia@sha256:11a9403ba099b1a7c34cd6a657c50c0fbf92e7f478afe95e34746e3b3b92de00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6.7-buster` - linux; amd64

```console
$ docker pull julia@sha256:487064e9ad24d34877e0e2048a33f74646d38a5f9cf8fdadba30fdcdcced7e21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154248703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b36fd9468d7d0e8a41bda44216d86d2ad7f03c3880c03c1296ad218fc15a42`
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
# Tue, 13 Sep 2022 06:11:07 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:11:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:11:22 GMT
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
	-	`sha256:99d42bcee1a8f29c6454067102ab79ef975bb5ce9e54677dcad8c23830d7b446`  
		Last Modified: Tue, 13 Sep 2022 06:14:15 GMT  
		Size: 122.6 MB (122649705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:983207dad9750fcd6194de9e3004a33f9b01849797d98ff6613b484c1914758b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140247878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56459e18d40e1d1770f76be018b9c466783bd627c4ccc1196751235696c77f8`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 03:43:14 GMT
ADD file:0a80cba5196c5f463d85aeb456ee0f5778155ac5b1d3ce93a2023f1141aac44a in / 
# Tue, 13 Sep 2022 03:43:14 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 11:42:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 11:42:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 11:42:18 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 11:42:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 11:42:18 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 11:42:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 11:42:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:04df89f99dde583959eeb3f2964381f6e5a3199fa335ea1b9862aab596638515`  
		Last Modified: Tue, 13 Sep 2022 03:50:50 GMT  
		Size: 22.7 MB (22740495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:521cd1df414e2cf557c09628189f6ec181fdae28a2f877040cc559890386a8eb`  
		Last Modified: Tue, 13 Sep 2022 11:43:41 GMT  
		Size: 3.8 MB (3811599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7168a35099c49997bc5a49c1ac3a8082b5ff384fb82391e9ed52921f978e3291`  
		Last Modified: Tue, 13 Sep 2022 11:44:04 GMT  
		Size: 113.7 MB (113695784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:56356e3b66a3e1fa183a329bab2ed7a38b2dfe3f4a3d8bf944dea753875c4eb1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146473259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f4e5e0ff633767d739da3ee78b599d3af08a47c338f956d64843f83439ee86`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:54:47 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 06:55:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:55:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa187f35c48ac07504837d6c194722424c0c81baca5ed508a23d828efc9666`  
		Last Modified: Tue, 13 Sep 2022 06:56:16 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2783963f8e1ea399bbc9bcaf86fd898dd341c177cd3cf525beb83d6e4a91f469`  
		Last Modified: Tue, 13 Sep 2022 06:57:39 GMT  
		Size: 116.2 MB (116222226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-buster` - linux; 386

```console
$ docker pull julia@sha256:974048b38530ab17ae42bad4d5daf40fff0dea006dfe0468d5af708fb5d265c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152511131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad37e35f5549af6c074a618052865f7055ac457d0d73c2ad01c12707d8a165`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:54 GMT
ENV JULIA_VERSION=1.6.7
# Tue, 13 Sep 2022 13:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:47:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a7b851a490ad11fdc5f9b5349c6e0938d538849e48fa0d16bcf71d7cd7b112`  
		Last Modified: Tue, 13 Sep 2022 13:48:27 GMT  
		Size: 4.6 MB (4616868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a608952f9b2635d6aa75c873099a6ca801fa330d9f5fff5dc0fa226eda98ca8`  
		Last Modified: Tue, 13 Sep 2022 13:49:44 GMT  
		Size: 120.1 MB (120103311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore`

```console
$ docker pull julia@sha256:4279aeb45596ea0abc3f53e4671560ec05f127b506ac2cf3f793862982c9523c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.6.7-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:644d19dcbfeafc426b55272d39aa9de0a726a26c787d76270a23a08975b8d906
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481594345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dd32d24916b20290b6bc6cac228d0494dca501603deb9e1800a4253582675f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:07:52 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:07:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:07:54 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:09:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c831f7593aee39d97551da204a861e05736dbc407f90afbc51129299ab39fb`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40644ea92254d602fe561f9820092bad40a2722661b9b9b1f198541b6b000ef5`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b42cf56bd8df7dc68e75819f671aac911872030a9878e313490278167ea4be6`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e55fdd6d2d2e7e18bc8ed2382d05ed462b678138437dbdfe16935fb1fd7aec`  
		Last Modified: Wed, 14 Sep 2022 15:37:20 GMT  
		Size: 134.6 MB (134637716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f9acec052a78ace03b0e9ff2822fa65a0c4d9bbbb20eb1dd76f82067d6a9`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:9f44d8acd087d17ab68d94cb6e05e7c4c68bf1c780c27500e5c3ea8b089b14ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e8cfeb87030fc9b54cedf3bbbf7cbee2d7b25b34d4e7fed60283bca7708b0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:09:35 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:09:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:09:37 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2220a85f440093d8ffc3dfceb27ffaa979230817172e729f0a4a89afc853d6`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1104e8b885c925dc4781d123b39f654d0c1681cd11a7a74017d396d798a9`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2790b7f1736a1ebb05e257efa31fe620c36a9ba22a3a094665ec328548fb45c`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfbe02615e95687de43ac0d5879b3b73bb23e3f8b108981a5141ac59f10a45`  
		Last Modified: Wed, 14 Sep 2022 15:37:59 GMT  
		Size: 134.4 MB (134422685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf99bd27c5c88bcb1c104ac4c6f9ac42c91645dba1962fcf29269f6da9b54e`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:b2e64d8c3e5ff5ebf70f50bd8c810dcff14af28dea451ec074545a5f96004a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:1.6.7-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:9f44d8acd087d17ab68d94cb6e05e7c4c68bf1c780c27500e5c3ea8b089b14ea
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837994499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e8cfeb87030fc9b54cedf3bbbf7cbee2d7b25b34d4e7fed60283bca7708b0d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:09:35 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:09:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:09:37 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:11:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:11:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2220a85f440093d8ffc3dfceb27ffaa979230817172e729f0a4a89afc853d6`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1104e8b885c925dc4781d123b39f654d0c1681cd11a7a74017d396d798a9`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2790b7f1736a1ebb05e257efa31fe620c36a9ba22a3a094665ec328548fb45c`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfbe02615e95687de43ac0d5879b3b73bb23e3f8b108981a5141ac59f10a45`  
		Last Modified: Wed, 14 Sep 2022 15:37:59 GMT  
		Size: 134.4 MB (134422685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bf99bd27c5c88bcb1c104ac4c6f9ac42c91645dba1962fcf29269f6da9b54e`  
		Last Modified: Wed, 14 Sep 2022 15:37:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:3acb97bc3707ad228c98b5ada87f6db6c75ca870226a7e2ca34fb2e346073e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:1.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:644d19dcbfeafc426b55272d39aa9de0a726a26c787d76270a23a08975b8d906
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2481594345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98dd32d24916b20290b6bc6cac228d0494dca501603deb9e1800a4253582675f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:07:52 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 14 Sep 2022 15:07:53 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 14 Sep 2022 15:07:54 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 14 Sep 2022 15:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:09:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c831f7593aee39d97551da204a861e05736dbc407f90afbc51129299ab39fb`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40644ea92254d602fe561f9820092bad40a2722661b9b9b1f198541b6b000ef5`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b42cf56bd8df7dc68e75819f671aac911872030a9878e313490278167ea4be6`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e55fdd6d2d2e7e18bc8ed2382d05ed462b678138437dbdfe16935fb1fd7aec`  
		Last Modified: Wed, 14 Sep 2022 15:37:20 GMT  
		Size: 134.6 MB (134637716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d74f9acec052a78ace03b0e9ff2822fa65a0c4d9bbbb20eb1dd76f82067d6a9`  
		Last Modified: Wed, 14 Sep 2022 15:36:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8`

```console
$ docker pull julia@sha256:937a26e034923edfc3c8a2dc5f0d5028e0f388b0790e7bc02de53c39d064fcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.8` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-alpine`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8-alpine` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-alpine3.15`

```console
$ docker pull julia@sha256:5a115d135d595fdb6f5cdba845f72eee906dd707e48de61eac72157ac2bf9941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:ff319b672dcbfd21237bb530ba7492aa01c9178a5218917d1b89170c7cfaa5ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c1754b206335a99b344bcc53aacfbb467c4b47f9ad4924de72226e29c04025`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:31:25 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0dfb1f33ed58261036c68d7560d680df65801f4b059a05fe06e948193369c`  
		Last Modified: Mon, 12 Sep 2022 22:34:49 GMT  
		Size: 149.3 MB (149258181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-alpine3.16`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-bullseye`

```console
$ docker pull julia@sha256:a6f06b8560c41b9bdf6b177f2a2dfe8d25a5bb7f026e7bc7f9e7d7c810bbd543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-bullseye` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-buster`

```console
$ docker pull julia@sha256:69fb0c560054f6a7b4188b0bfde186950f4904eb6bfad43546e5391ca9cfd6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8-buster` - linux; amd64

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

### `julia:1.8-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:057b284350db760bc44819f2909cb2f8a95a9a694390e5e01871d6e36c11d78d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171524573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d93b15ca1982cbcc1b02ab350119160e5af7041bd09f3bdcb22da8adbdc841d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:54:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa187f35c48ac07504837d6c194722424c0c81baca5ed508a23d828efc9666`  
		Last Modified: Tue, 13 Sep 2022 06:56:16 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc66ab2dccb76145b27255e0261d2f25bce448781874c0a7cf876fe84f79f7`  
		Last Modified: Tue, 13 Sep 2022 06:56:37 GMT  
		Size: 141.3 MB (141273540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-buster` - linux; 386

```console
$ docker pull julia@sha256:2240953ec1fef6783d4117f4a75f16ac5a59b22323cffc5b39c56d92128f5aaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176846643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0fb2fa1e54f4a3754ecb337c1477c3d30067cecad272941d154393d52f7981`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:00 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:46:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a7b851a490ad11fdc5f9b5349c6e0938d538849e48fa0d16bcf71d7cd7b112`  
		Last Modified: Tue, 13 Sep 2022 13:48:27 GMT  
		Size: 4.6 MB (4616868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f253c99ab3897bca0e37018c75ff6189c2bac9d9489b35d6f05b2e04a3b28`  
		Last Modified: Tue, 13 Sep 2022 13:48:45 GMT  
		Size: 144.4 MB (144438823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-windowsservercore`

```console
$ docker pull julia@sha256:4e88e4f8e75b83804369da22e073a4b4ee182786184554f0f7fe4bdac80a4a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.8-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-windowsservercore-1809`

```console
$ docker pull julia@sha256:f21df5147ee24f953f369cca1661278da236866aeb2351a84d5afcbe0dc47a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:1.8-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:12dfddf543c66c842e918b5c92bdb2da960d977556a2a4f65c9a6476a1146543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:1.8-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1`

```console
$ docker pull julia@sha256:937a26e034923edfc3c8a2dc5f0d5028e0f388b0790e7bc02de53c39d064fcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.8.1` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-alpine`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8.1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-alpine3.15`

```console
$ docker pull julia@sha256:5a115d135d595fdb6f5cdba845f72eee906dd707e48de61eac72157ac2bf9941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8.1-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:ff319b672dcbfd21237bb530ba7492aa01c9178a5218917d1b89170c7cfaa5ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c1754b206335a99b344bcc53aacfbb467c4b47f9ad4924de72226e29c04025`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:31:25 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0dfb1f33ed58261036c68d7560d680df65801f4b059a05fe06e948193369c`  
		Last Modified: Mon, 12 Sep 2022 22:34:49 GMT  
		Size: 149.3 MB (149258181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-alpine3.16`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8.1-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-bullseye`

```console
$ docker pull julia@sha256:a6f06b8560c41b9bdf6b177f2a2dfe8d25a5bb7f026e7bc7f9e7d7c810bbd543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8.1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-buster`

```console
$ docker pull julia@sha256:69fb0c560054f6a7b4188b0bfde186950f4904eb6bfad43546e5391ca9cfd6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8.1-buster` - linux; amd64

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

### `julia:1.8.1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:057b284350db760bc44819f2909cb2f8a95a9a694390e5e01871d6e36c11d78d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171524573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d93b15ca1982cbcc1b02ab350119160e5af7041bd09f3bdcb22da8adbdc841d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:54:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa187f35c48ac07504837d6c194722424c0c81baca5ed508a23d828efc9666`  
		Last Modified: Tue, 13 Sep 2022 06:56:16 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc66ab2dccb76145b27255e0261d2f25bce448781874c0a7cf876fe84f79f7`  
		Last Modified: Tue, 13 Sep 2022 06:56:37 GMT  
		Size: 141.3 MB (141273540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1-buster` - linux; 386

```console
$ docker pull julia@sha256:2240953ec1fef6783d4117f4a75f16ac5a59b22323cffc5b39c56d92128f5aaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176846643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0fb2fa1e54f4a3754ecb337c1477c3d30067cecad272941d154393d52f7981`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:00 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:46:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a7b851a490ad11fdc5f9b5349c6e0938d538849e48fa0d16bcf71d7cd7b112`  
		Last Modified: Tue, 13 Sep 2022 13:48:27 GMT  
		Size: 4.6 MB (4616868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f253c99ab3897bca0e37018c75ff6189c2bac9d9489b35d6f05b2e04a3b28`  
		Last Modified: Tue, 13 Sep 2022 13:48:45 GMT  
		Size: 144.4 MB (144438823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-windowsservercore`

```console
$ docker pull julia@sha256:4e88e4f8e75b83804369da22e073a4b4ee182786184554f0f7fe4bdac80a4a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:1.8.1-windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.1-windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-windowsservercore-1809`

```console
$ docker pull julia@sha256:f21df5147ee24f953f369cca1661278da236866aeb2351a84d5afcbe0dc47a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:1.8.1-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:12dfddf543c66c842e918b5c92bdb2da960d977556a2a4f65c9a6476a1146543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:1.8.1-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine3.15`

```console
$ docker pull julia@sha256:5a115d135d595fdb6f5cdba845f72eee906dd707e48de61eac72157ac2bf9941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:ff319b672dcbfd21237bb530ba7492aa01c9178a5218917d1b89170c7cfaa5ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152081693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c1754b206335a99b344bcc53aacfbb467c4b47f9ad4924de72226e29c04025`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:31:25 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e0dfb1f33ed58261036c68d7560d680df65801f4b059a05fe06e948193369c`  
		Last Modified: Mon, 12 Sep 2022 22:34:49 GMT  
		Size: 149.3 MB (149258181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine3.16`

```console
$ docker pull julia@sha256:fac15652a6c07605ea777b892df34b61dc2c8ecdbd091d5a73525e2b2c3fae08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:e711ec5666450576c1bf0d7ff1073f01a3efefce2742267130870d25275464df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152064487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e606f4ad058113d6e2c4b37c28dc0ecd6cbc0ce05c2ee38e316f29a4e491bcb9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Aug 2022 20:42:34 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 20:42:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 12 Sep 2022 22:30:57 GMT
ENV JULIA_VERSION=1.8.1
# Mon, 12 Sep 2022 22:31:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.1-musl-x86_64.tar.gz'; 			sha256='d459b1283401a51219d619ecb053920be68b2331eb239e68c9c3a87a2388f4c4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Mon, 12 Sep 2022 22:31:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d5077780a65658451435cb2305d83206f4c58db4599de6934b9162367ee5492`  
		Last Modified: Mon, 12 Sep 2022 22:34:03 GMT  
		Size: 149.3 MB (149258433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bullseye`

```console
$ docker pull julia@sha256:a6f06b8560c41b9bdf6b177f2a2dfe8d25a5bb7f026e7bc7f9e7d7c810bbd543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:buster`

```console
$ docker pull julia@sha256:69fb0c560054f6a7b4188b0bfde186950f4904eb6bfad43546e5391ca9cfd6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

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

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:057b284350db760bc44819f2909cb2f8a95a9a694390e5e01871d6e36c11d78d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171524573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d93b15ca1982cbcc1b02ab350119160e5af7041bd09f3bdcb22da8adbdc841d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:11:20 GMT
ADD file:18fa3591fcbf0c3e065dbe581a069fc2af6fab9e4446047348404881af960725 in / 
# Tue, 13 Sep 2022 02:11:21 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:54:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:54:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c3f5cce277263c7aeaf67f83255af76927e03363e775f39d7587bc5036fcf1e`  
		Last Modified: Tue, 13 Sep 2022 02:17:10 GMT  
		Size: 25.9 MB (25904152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffaa187f35c48ac07504837d6c194722424c0c81baca5ed508a23d828efc9666`  
		Last Modified: Tue, 13 Sep 2022 06:56:16 GMT  
		Size: 4.3 MB (4346881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc66ab2dccb76145b27255e0261d2f25bce448781874c0a7cf876fe84f79f7`  
		Last Modified: Tue, 13 Sep 2022 06:56:37 GMT  
		Size: 141.3 MB (141273540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:2240953ec1fef6783d4117f4a75f16ac5a59b22323cffc5b39c56d92128f5aaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.8 MB (176846643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0fb2fa1e54f4a3754ecb337c1477c3d30067cecad272941d154393d52f7981`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:40:12 GMT
ADD file:da95249e10828562612e8b0a3595f3cbf6a5cb5dbfb47302a4d42a4a8c5025b1 in / 
# Tue, 13 Sep 2022 01:40:12 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:46:00 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:46:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:46:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7db2238a0cb6ea85529a33cb395b0243796e76066f31656ba5e08232e2fb0308`  
		Last Modified: Tue, 13 Sep 2022 01:46:12 GMT  
		Size: 27.8 MB (27790952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a7b851a490ad11fdc5f9b5349c6e0938d538849e48fa0d16bcf71d7cd7b112`  
		Last Modified: Tue, 13 Sep 2022 13:48:27 GMT  
		Size: 4.6 MB (4616868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52f253c99ab3897bca0e37018c75ff6189c2bac9d9489b35d6f05b2e04a3b28`  
		Last Modified: Tue, 13 Sep 2022 13:48:45 GMT  
		Size: 144.4 MB (144438823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:latest`

```console
$ docker pull julia@sha256:937a26e034923edfc3c8a2dc5f0d5028e0f388b0790e7bc02de53c39d064fcc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:312df84945af6522874c826fafbce96cf604f6637b9c539fcf06a76fa3d72715
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181487209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c96681f1f7741cafe4fcc5e17bcd4e6473848f3f7edbf51e976cea8e7be5164`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:09:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:09:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:09:51 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:10:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:10:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb0ea27551b6102160334e014f439121e3175e068ebf941694b630b054cffe`  
		Last Modified: Tue, 13 Sep 2022 06:12:05 GMT  
		Size: 2.4 MB (2426572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63662fd2235007a78da621e2a5e7c18de2064de2c9447edf6ae02fcc4b3e6590`  
		Last Modified: Tue, 13 Sep 2022 06:12:27 GMT  
		Size: 147.7 MB (147656516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:338899e67d0f21a9a5750baa01c295c04458e0fa6fc1c34bbcabb17778b000af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173728205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b175543485c3524f84995cfdbd60e954947107acd72222c75d542227933d490`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 02:10:56 GMT
ADD file:e8f00260a993aacae732bef51e6074b6c064d50a8ce1f0c44d53fe9e3c868e43 in / 
# Tue, 13 Sep 2022 02:10:56 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 06:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 06:53:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 06:53:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 06:53:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 06:53:17 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 06:53:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 06:53:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3d898485473e3507374cea2e09f019c2ff5728f0911aa36c70b7a7235e9bc8ac`  
		Last Modified: Tue, 13 Sep 2022 02:16:19 GMT  
		Size: 30.1 MB (30054239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d002c992f414748438c80c04c60af98ef015e1bb23834a3ca2c83bbda6b212`  
		Last Modified: Tue, 13 Sep 2022 06:55:38 GMT  
		Size: 2.4 MB (2413689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367b330f78697fc504126dba42ee45ae6f9c2f87b54b029db0ca42f486e05d77`  
		Last Modified: Tue, 13 Sep 2022 06:55:59 GMT  
		Size: 141.3 MB (141260277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:7d031ee27629be1be27a942895499e355409711c9527a2e1ab8f7f66e11320c8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179349962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9a25f84856c5782e415a889decd82ff27866453b3039f50ef99e88dc70b95f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 13 Sep 2022 01:39:44 GMT
ADD file:414dad8d6231b19eca031ae43d450f7b700460907f7319c029b542ab528c5f9b in / 
# Tue, 13 Sep 2022 01:39:45 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:45:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:45:18 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 13 Sep 2022 13:45:19 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Sep 2022 13:45:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 13 Sep 2022 13:45:21 GMT
ENV JULIA_VERSION=1.8.1
# Tue, 13 Sep 2022 13:45:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.1-linux-x86_64.tar.gz'; 			sha256='33054ee647ee8a4fb54fc05110e07e0b53e04591fe53d0a4cb4c7ed7a05e91f1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.1-linux-aarch64.tar.gz'; 			sha256='ba06837ac2899547bbb799989f11464fecd6782226871c3b7a48619481042679'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.1-linux-i686.tar.gz'; 			sha256='975139acd9889c4db1e4d0945abe90f9c6b03ee3882837aa4b3e561d9c7f75a7'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 13 Sep 2022 13:45:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:221c5dcdb82ed8982a21341b5c0cadf79cc338347a649dc99854a5697661d7aa`  
		Last Modified: Tue, 13 Sep 2022 01:45:21 GMT  
		Size: 32.4 MB (32383788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6a6ce58cad705a2099d8d869fb92cbb0bee1ed3f63afc77d62ed27cf3e2d9e`  
		Last Modified: Tue, 13 Sep 2022 13:47:50 GMT  
		Size: 2.5 MB (2531745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce59e8e159d1341b3dfe2e8892671ac34eaf6c777208859adcb941dcafea980`  
		Last Modified: Tue, 13 Sep 2022 13:48:08 GMT  
		Size: 144.4 MB (144434429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:4e88e4f8e75b83804369da22e073a4b4ee182786184554f0f7fe4bdac80a4a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `julia:windowsservercore` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:f21df5147ee24f953f369cca1661278da236866aeb2351a84d5afcbe0dc47a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:12dfddf543c66c842e918b5c92bdb2da960d977556a2a4f65c9a6476a1146543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
