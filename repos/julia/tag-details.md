<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-alpine`](#julia1-alpine)
-	[`julia:1-alpine3.14`](#julia1-alpine314)
-	[`julia:1-alpine3.15`](#julia1-alpine315)
-	[`julia:1-bullseye`](#julia1-bullseye)
-	[`julia:1-buster`](#julia1-buster)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2016`](#julia1-windowsservercore-ltsc2016)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1.6`](#julia16)
-	[`julia:1.6-alpine`](#julia16-alpine)
-	[`julia:1.6-alpine3.14`](#julia16-alpine314)
-	[`julia:1.6-alpine3.15`](#julia16-alpine315)
-	[`julia:1.6-bullseye`](#julia16-bullseye)
-	[`julia:1.6-buster`](#julia16-buster)
-	[`julia:1.6-windowsservercore`](#julia16-windowsservercore)
-	[`julia:1.6-windowsservercore-1809`](#julia16-windowsservercore-1809)
-	[`julia:1.6-windowsservercore-ltsc2016`](#julia16-windowsservercore-ltsc2016)
-	[`julia:1.6-windowsservercore-ltsc2022`](#julia16-windowsservercore-ltsc2022)
-	[`julia:1.6.4`](#julia164)
-	[`julia:1.6.4-alpine`](#julia164-alpine)
-	[`julia:1.6.4-alpine3.14`](#julia164-alpine314)
-	[`julia:1.6.4-alpine3.15`](#julia164-alpine315)
-	[`julia:1.6.4-bullseye`](#julia164-bullseye)
-	[`julia:1.6.4-buster`](#julia164-buster)
-	[`julia:1.6.4-windowsservercore`](#julia164-windowsservercore)
-	[`julia:1.6.4-windowsservercore-1809`](#julia164-windowsservercore-1809)
-	[`julia:1.6.4-windowsservercore-ltsc2016`](#julia164-windowsservercore-ltsc2016)
-	[`julia:1.6.4-windowsservercore-ltsc2022`](#julia164-windowsservercore-ltsc2022)
-	[`julia:1.7`](#julia17)
-	[`julia:1.7-alpine`](#julia17-alpine)
-	[`julia:1.7-alpine3.14`](#julia17-alpine314)
-	[`julia:1.7-alpine3.15`](#julia17-alpine315)
-	[`julia:1.7-bullseye`](#julia17-bullseye)
-	[`julia:1.7-buster`](#julia17-buster)
-	[`julia:1.7-windowsservercore`](#julia17-windowsservercore)
-	[`julia:1.7-windowsservercore-1809`](#julia17-windowsservercore-1809)
-	[`julia:1.7-windowsservercore-ltsc2016`](#julia17-windowsservercore-ltsc2016)
-	[`julia:1.7-windowsservercore-ltsc2022`](#julia17-windowsservercore-ltsc2022)
-	[`julia:1.7.0`](#julia170)
-	[`julia:1.7.0-alpine`](#julia170-alpine)
-	[`julia:1.7.0-alpine3.14`](#julia170-alpine314)
-	[`julia:1.7.0-alpine3.15`](#julia170-alpine315)
-	[`julia:1.7.0-bullseye`](#julia170-bullseye)
-	[`julia:1.7.0-buster`](#julia170-buster)
-	[`julia:1.7.0-windowsservercore`](#julia170-windowsservercore)
-	[`julia:1.7.0-windowsservercore-1809`](#julia170-windowsservercore-1809)
-	[`julia:1.7.0-windowsservercore-ltsc2016`](#julia170-windowsservercore-ltsc2016)
-	[`julia:1.7.0-windowsservercore-ltsc2022`](#julia170-windowsservercore-ltsc2022)
-	[`julia:alpine`](#juliaalpine)
-	[`julia:alpine3.14`](#juliaalpine314)
-	[`julia:alpine3.15`](#juliaalpine315)
-	[`julia:bullseye`](#juliabullseye)
-	[`julia:buster`](#juliabuster)
-	[`julia:latest`](#julialatest)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2016`](#juliawindowsservercore-ltsc2016)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)

## `julia:1`

```console
$ docker pull julia@sha256:6813817da8dd4de68259d62eb0a685c351353a69de15c02d631305b13d7fb09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine3.14`

```console
$ docker pull julia@sha256:72db22e0f6ee8dd6bf15f47d6d9102978a39b82a5213a88d74e8ab5ddd58e559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.14` - linux; amd64

```console
$ docker pull julia@sha256:7bd37afd83771132a076c628443e911613188fd38ed69730e83ad29ac3405f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123721967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88e667c7049e11b615b66bb6fa709f2216d2d03c0518ad9b7dbf12d04d2247`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 13 Nov 2021 06:02:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:02:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 23 Nov 2021 01:26:57 GMT
ENV JULIA_VERSION=1.6.4
# Tue, 23 Nov 2021 01:27:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 23 Nov 2021 01:27:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2f4ada6a836ddc6aad395d8b5de36bd7772c412b43bf6fa5f6f8ab4104b1cc`  
		Last Modified: Tue, 23 Nov 2021 01:29:22 GMT  
		Size: 120.9 MB (120898986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine3.15`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:d71c37dc6cdfa071d88b2680feb47cf922f26d668a372162bf7ef11d211b1052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-buster`

```console
$ docker pull julia@sha256:87116c86344cf4ab009df1411b870b2024d3445302c61d54b4555a68806f3f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:48937060ff93ae448b072263d61ee808be1594185bbaa9fadced6db42be29bb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153286261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707777fd72fc7c14d1d3a6935c33af074d56a91f2da13e6593a82cf6a0a9d6fc`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:53 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:44:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:44:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20759da86ee815c76ac66ee463388da4394f7392c03224943a2bd16dc7465c61`  
		Last Modified: Thu, 02 Dec 2021 09:46:46 GMT  
		Size: 4.5 MB (4458542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e35e44e68ba9806eebf32f56ea1f3330676ef3c8e13e26b494a91936e4979`  
		Last Modified: Thu, 02 Dec 2021 09:48:30 GMT  
		Size: 121.7 MB (121673990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d9bdb79d807b1654c98525102b535d4d0b94804df9d95143b2d6cd928edf9816
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145549008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba06cb918bf1e3309fb0182c522a5a2fcd6484af3fa337a83bbbb759a6b9b0b7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:44 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:22:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613768401ba4c98b7337eb641463cbd04d29d049c55cf47a4a732e5d16c6aa37`  
		Last Modified: Thu, 02 Dec 2021 10:24:14 GMT  
		Size: 4.3 MB (4338201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b2bba91454eb6c5b227df7159f1129ae22ba1e4c93bf637397e8e08773260`  
		Last Modified: Thu, 02 Dec 2021 10:25:41 GMT  
		Size: 115.3 MB (115287663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:6bc17f6e123e101929161a8e67d663644969aabd0248224949638ad252200a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161067535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fb7fe2bf06607e7cbf03841302b886b4e49515b81cd3dcb86642638a17db49`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:20:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:57:22 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c1c092d2a055f47d0a8f69b9a68445f7be8dd96e7cb88a4987b4594b06e10`  
		Last Modified: Thu, 02 Dec 2021 09:24:11 GMT  
		Size: 4.6 MB (4610923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449dabd2d773251d9f33948c89c9e48edf3d7b67efbf2531f849bfbabd8c5676`  
		Last Modified: Fri, 03 Dec 2021 12:00:52 GMT  
		Size: 128.7 MB (128652050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:ddc566b528620adc3b6c879091d20577ef2884a92f70e18f7f09249d9005bd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:0610b340222e87e165f1ef09d5d94552f085371a0ce548b8954fd2bb2ead3cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:10e088aad15e9619bbf141e37f769c15a2d799c98156d71ea47aef15072617c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:1-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:65bdc4b753a26cdc05f71ea5c9e792a8bdbe771da35eee7fb96c58ef5b90f0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6`

```console
$ docker pull julia@sha256:af1ab40b5e90de0a0624d6c728059e24864e6a8477f14f5f980efaf2ea5a2bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.6` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; arm variant v7

```console
$ docker pull julia@sha256:41e985be7812b17b0f4d3a56c1e3e4c222b095604cdeb963dac28eec963f7148
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141695789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfeac8808213d9adbd26ef9c7717f85bd0e09a33c9ae6753054411f52cf9c7e`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 15:54:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 15:54:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 15:54:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 15:56:52 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 15:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 15:57:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba63f25775a4379e7a82358784a81f364a27c1fbd66d62920077fe305269f65`  
		Last Modified: Thu, 02 Dec 2021 16:02:43 GMT  
		Size: 2.2 MB (2227515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f80d5905455bc4087e33d9e3b560522a954e582437d0e20b06768773d0c1a4`  
		Last Modified: Thu, 02 Dec 2021 16:07:06 GMT  
		Size: 112.9 MB (112895082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; 386

```console
$ docker pull julia@sha256:1c24c1394ba495236f0d8dfe723cf64827b13a316b2305d1d9697f9eca652459
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154239864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44a5cd5485bc2f27fc41f13c0d97004af292f4da76776b7543fe62d777d8728`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:20:28 GMT
ENV JULIA_VERSION=1.6.4
# Fri, 03 Dec 2021 11:58:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.4-linux-x86_64.tar.gz'; 			sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.4-linux-armv7l.tar.gz'; 			sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.4-linux-aarch64.tar.gz'; 			sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.4-linux-i686.tar.gz'; 			sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:58:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7823bdf5cf6b356fe4872c3aa19ec265a27cd8fc8cfae3fe886748a7cb422c8`  
		Last Modified: Fri, 03 Dec 2021 12:01:34 GMT  
		Size: 119.3 MB (119329476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:e31f82ce278fcc6285fce308fcb27f0ce5608c206fb552f2ff9bdc462884ede1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318892430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f30e0ce66728515a9abad756ed5b4d101a0cf27ebd98e2205ead99e4f21377`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:15:15 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:23:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:23:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353751959e1e07e0824a3e57fbaa27d0fca8182b502a237f1794b51e491eaf`  
		Last Modified: Tue, 23 Nov 2021 01:22:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8f625347e49af87560b5503ce4cbe1f2b742c43e8ea07dcb0b32452f0aef2`  
		Last Modified: Thu, 02 Dec 2021 20:35:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f58ca42bf8632a09f4cb77c525516e4f2a1fb7ff113bbc462a70a339c900b6f`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fb13589da407a458f7a67290bba0136349e0816c8bf910fd2fe26f0f45720`  
		Last Modified: Thu, 02 Dec 2021 20:38:13 GMT  
		Size: 134.3 MB (134278364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f506237e45790a885a47c45fd9b86175d3b3fe522499bca246f31db841fa3`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:7f36857f78e873e0487424cafa6404bd9009bf38de7470148cee97e52708c3fe
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840183654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e337791a90f19f1bdb55d17453b539366760d77ab304e50d42bb5dc69dcd322`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:16:57 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:23:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:23:51 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:25:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb41f4249d9110eae98c897d297b7ae5d9988bd70dabb4157834c6a4c831907`  
		Last Modified: Tue, 23 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2084c07ff3b28baf268b3d8a1ebdbbe165abfa7557b5c7c226eacabc29c1cf57`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f16be292122f56fd1c53e7510ff183edbad6c65758d300350c3851299ab15c`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94b44743ed005bb9430b0f2b89bc2094fcc5c8516d9921b0a417a9719505f3`  
		Last Modified: Thu, 02 Dec 2021 20:40:50 GMT  
		Size: 134.1 MB (134055514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8c1484f5aa43fa4cb9c4a62c541d048b63be8cc958b2c4b61d412feb2b3470`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:0493a28099b79eae4c9ad622afa014a6d19f6599af08bcc70964bdee33ed2fc1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6407126107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689a1e5c1e173b847ee7fae035c8f1766de55b2c621cc9fe9976a91e34bde733`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:19:24 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:26:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:26:18 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:28:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567970bba379bc9d0742b8793b03e90ffa89398328348fbecd4190381c348917`  
		Last Modified: Tue, 23 Nov 2021 01:24:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104d6d41e17afac4422e3e2be3e6957ecb5bed454bd552176673c7b5e90504a`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee1642c2dc852454e8048e6a6efc9a3820c686d0b799c932b4abad59e69fb6`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e665ccea7290062b33ad896ba3b86ab64ca3bde1aa5d570e04d5c0a96912b77e`  
		Last Modified: Thu, 02 Dec 2021 20:41:30 GMT  
		Size: 134.0 MB (134028484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42054a0452ef38dc7117a8c502f3117ab8c0a00ab6b183aeff5d947bf35ba94`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine3.14`

```console
$ docker pull julia@sha256:72db22e0f6ee8dd6bf15f47d6d9102978a39b82a5213a88d74e8ab5ddd58e559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine3.14` - linux; amd64

```console
$ docker pull julia@sha256:7bd37afd83771132a076c628443e911613188fd38ed69730e83ad29ac3405f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123721967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88e667c7049e11b615b66bb6fa709f2216d2d03c0518ad9b7dbf12d04d2247`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 13 Nov 2021 06:02:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:02:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 23 Nov 2021 01:26:57 GMT
ENV JULIA_VERSION=1.6.4
# Tue, 23 Nov 2021 01:27:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 23 Nov 2021 01:27:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2f4ada6a836ddc6aad395d8b5de36bd7772c412b43bf6fa5f6f8ab4104b1cc`  
		Last Modified: Tue, 23 Nov 2021 01:29:22 GMT  
		Size: 120.9 MB (120898986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine3.15`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-bullseye`

```console
$ docker pull julia@sha256:4cb8cd7d4062e7be1f2579bf200b27333b4225a1d2eb2ad85883217e45e3bf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:41e985be7812b17b0f4d3a56c1e3e4c222b095604cdeb963dac28eec963f7148
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141695789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfeac8808213d9adbd26ef9c7717f85bd0e09a33c9ae6753054411f52cf9c7e`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 15:54:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 15:54:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 15:54:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 15:56:52 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 15:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 15:57:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba63f25775a4379e7a82358784a81f364a27c1fbd66d62920077fe305269f65`  
		Last Modified: Thu, 02 Dec 2021 16:02:43 GMT  
		Size: 2.2 MB (2227515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f80d5905455bc4087e33d9e3b560522a954e582437d0e20b06768773d0c1a4`  
		Last Modified: Thu, 02 Dec 2021 16:07:06 GMT  
		Size: 112.9 MB (112895082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; 386

```console
$ docker pull julia@sha256:1c24c1394ba495236f0d8dfe723cf64827b13a316b2305d1d9697f9eca652459
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154239864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44a5cd5485bc2f27fc41f13c0d97004af292f4da76776b7543fe62d777d8728`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:20:28 GMT
ENV JULIA_VERSION=1.6.4
# Fri, 03 Dec 2021 11:58:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.4-linux-x86_64.tar.gz'; 			sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.4-linux-armv7l.tar.gz'; 			sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.4-linux-aarch64.tar.gz'; 			sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.4-linux-i686.tar.gz'; 			sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:58:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7823bdf5cf6b356fe4872c3aa19ec265a27cd8fc8cfae3fe886748a7cb422c8`  
		Last Modified: Fri, 03 Dec 2021 12:01:34 GMT  
		Size: 119.3 MB (119329476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-buster`

```console
$ docker pull julia@sha256:b932e93045fcbcebc4181654f3f6d641839d2c95c0158d5616b6e3fbb4bcd957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6-buster` - linux; amd64

```console
$ docker pull julia@sha256:48937060ff93ae448b072263d61ee808be1594185bbaa9fadced6db42be29bb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153286261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707777fd72fc7c14d1d3a6935c33af074d56a91f2da13e6593a82cf6a0a9d6fc`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:53 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:44:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:44:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20759da86ee815c76ac66ee463388da4394f7392c03224943a2bd16dc7465c61`  
		Last Modified: Thu, 02 Dec 2021 09:46:46 GMT  
		Size: 4.5 MB (4458542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e35e44e68ba9806eebf32f56ea1f3330676ef3c8e13e26b494a91936e4979`  
		Last Modified: Thu, 02 Dec 2021 09:48:30 GMT  
		Size: 121.7 MB (121673990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:2d765975c8a4cfa884b10d2ba0a9ce8b215d11a4fba8b85c821a8a5c60a2aba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139468568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e00876aecfc2bd801918c448805ee9b2675b8b75222c10ca490c908c5c3706`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 15:55:52 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 15:55:52 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 15:55:53 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 15:58:07 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 15:58:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 15:58:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135ada6a5e8fe302e1e9ef466d0da0cc87d2339e25533cb08a044bd660165fa6`  
		Last Modified: Thu, 02 Dec 2021 16:04:23 GMT  
		Size: 3.8 MB (3806048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661f743504ec29bd6b040e2203b21eccc28169a65d7ce2e943132a00df724a7d`  
		Last Modified: Thu, 02 Dec 2021 16:08:39 GMT  
		Size: 112.9 MB (112908155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d9bdb79d807b1654c98525102b535d4d0b94804df9d95143b2d6cd928edf9816
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145549008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba06cb918bf1e3309fb0182c522a5a2fcd6484af3fa337a83bbbb759a6b9b0b7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:44 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:22:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613768401ba4c98b7337eb641463cbd04d29d049c55cf47a4a732e5d16c6aa37`  
		Last Modified: Thu, 02 Dec 2021 10:24:14 GMT  
		Size: 4.3 MB (4338201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b2bba91454eb6c5b227df7159f1129ae22ba1e4c93bf637397e8e08773260`  
		Last Modified: Thu, 02 Dec 2021 10:25:41 GMT  
		Size: 115.3 MB (115287663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; 386

```console
$ docker pull julia@sha256:856061600bc6474418865589e5254ab378ba945628030b83ea4828d1fdae2a97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151748633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8726472cb16289c1e43d37ec17eed80e849dbc26ceac3260460092e183f471ec`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:20:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:21:02 GMT
ENV JULIA_VERSION=1.6.4
# Fri, 03 Dec 2021 11:58:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.4-linux-x86_64.tar.gz'; 			sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.4-linux-armv7l.tar.gz'; 			sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.4-linux-aarch64.tar.gz'; 			sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.4-linux-i686.tar.gz'; 			sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:58:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c1c092d2a055f47d0a8f69b9a68445f7be8dd96e7cb88a4987b4594b06e10`  
		Last Modified: Thu, 02 Dec 2021 09:24:11 GMT  
		Size: 4.6 MB (4610923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9106b7ba6db81bd4f3eb2549efc07d0c60d3c692318685991e5e31e7021f9d`  
		Last Modified: Fri, 03 Dec 2021 12:02:17 GMT  
		Size: 119.3 MB (119333148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore`

```console
$ docker pull julia@sha256:4ab0a749878e8689f2922f74cf40862a340611eddfdd35d21c7a2c6fdff1ff78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.6-windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:e31f82ce278fcc6285fce308fcb27f0ce5608c206fb552f2ff9bdc462884ede1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318892430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f30e0ce66728515a9abad756ed5b4d101a0cf27ebd98e2205ead99e4f21377`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:15:15 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:23:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:23:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353751959e1e07e0824a3e57fbaa27d0fca8182b502a237f1794b51e491eaf`  
		Last Modified: Tue, 23 Nov 2021 01:22:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8f625347e49af87560b5503ce4cbe1f2b742c43e8ea07dcb0b32452f0aef2`  
		Last Modified: Thu, 02 Dec 2021 20:35:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f58ca42bf8632a09f4cb77c525516e4f2a1fb7ff113bbc462a70a339c900b6f`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fb13589da407a458f7a67290bba0136349e0816c8bf910fd2fe26f0f45720`  
		Last Modified: Thu, 02 Dec 2021 20:38:13 GMT  
		Size: 134.3 MB (134278364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f506237e45790a885a47c45fd9b86175d3b3fe522499bca246f31db841fa3`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:7f36857f78e873e0487424cafa6404bd9009bf38de7470148cee97e52708c3fe
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840183654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e337791a90f19f1bdb55d17453b539366760d77ab304e50d42bb5dc69dcd322`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:16:57 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:23:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:23:51 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:25:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb41f4249d9110eae98c897d297b7ae5d9988bd70dabb4157834c6a4c831907`  
		Last Modified: Tue, 23 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2084c07ff3b28baf268b3d8a1ebdbbe165abfa7557b5c7c226eacabc29c1cf57`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f16be292122f56fd1c53e7510ff183edbad6c65758d300350c3851299ab15c`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94b44743ed005bb9430b0f2b89bc2094fcc5c8516d9921b0a417a9719505f3`  
		Last Modified: Thu, 02 Dec 2021 20:40:50 GMT  
		Size: 134.1 MB (134055514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8c1484f5aa43fa4cb9c4a62c541d048b63be8cc958b2c4b61d412feb2b3470`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:0493a28099b79eae4c9ad622afa014a6d19f6599af08bcc70964bdee33ed2fc1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6407126107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689a1e5c1e173b847ee7fae035c8f1766de55b2c621cc9fe9976a91e34bde733`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:19:24 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:26:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:26:18 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:28:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567970bba379bc9d0742b8793b03e90ffa89398328348fbecd4190381c348917`  
		Last Modified: Tue, 23 Nov 2021 01:24:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104d6d41e17afac4422e3e2be3e6957ecb5bed454bd552176673c7b5e90504a`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee1642c2dc852454e8048e6a6efc9a3820c686d0b799c932b4abad59e69fb6`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e665ccea7290062b33ad896ba3b86ab64ca3bde1aa5d570e04d5c0a96912b77e`  
		Last Modified: Thu, 02 Dec 2021 20:41:30 GMT  
		Size: 134.0 MB (134028484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42054a0452ef38dc7117a8c502f3117ab8c0a00ab6b183aeff5d947bf35ba94`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:9a34215480e787fb91592a090f9539faa35b77399a578423e44b75c8d6d523ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `julia:1.6-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:7f36857f78e873e0487424cafa6404bd9009bf38de7470148cee97e52708c3fe
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840183654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e337791a90f19f1bdb55d17453b539366760d77ab304e50d42bb5dc69dcd322`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:16:57 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:23:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:23:51 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:25:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb41f4249d9110eae98c897d297b7ae5d9988bd70dabb4157834c6a4c831907`  
		Last Modified: Tue, 23 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2084c07ff3b28baf268b3d8a1ebdbbe165abfa7557b5c7c226eacabc29c1cf57`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f16be292122f56fd1c53e7510ff183edbad6c65758d300350c3851299ab15c`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94b44743ed005bb9430b0f2b89bc2094fcc5c8516d9921b0a417a9719505f3`  
		Last Modified: Thu, 02 Dec 2021 20:40:50 GMT  
		Size: 134.1 MB (134055514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8c1484f5aa43fa4cb9c4a62c541d048b63be8cc958b2c4b61d412feb2b3470`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:0b4c54b82e6bfa89d3bbc41a07bf6bc31858bed9915ff75fe1998b605477efef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:1.6-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:0493a28099b79eae4c9ad622afa014a6d19f6599af08bcc70964bdee33ed2fc1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6407126107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689a1e5c1e173b847ee7fae035c8f1766de55b2c621cc9fe9976a91e34bde733`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:19:24 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:26:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:26:18 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:28:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567970bba379bc9d0742b8793b03e90ffa89398328348fbecd4190381c348917`  
		Last Modified: Tue, 23 Nov 2021 01:24:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104d6d41e17afac4422e3e2be3e6957ecb5bed454bd552176673c7b5e90504a`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee1642c2dc852454e8048e6a6efc9a3820c686d0b799c932b4abad59e69fb6`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e665ccea7290062b33ad896ba3b86ab64ca3bde1aa5d570e04d5c0a96912b77e`  
		Last Modified: Thu, 02 Dec 2021 20:41:30 GMT  
		Size: 134.0 MB (134028484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42054a0452ef38dc7117a8c502f3117ab8c0a00ab6b183aeff5d947bf35ba94`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c4554404ef73bd92d07269b857ce44bffeaf775a45541becaeb2a1bb82bf91e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `julia:1.6-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:e31f82ce278fcc6285fce308fcb27f0ce5608c206fb552f2ff9bdc462884ede1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318892430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f30e0ce66728515a9abad756ed5b4d101a0cf27ebd98e2205ead99e4f21377`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:15:15 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:23:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:23:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353751959e1e07e0824a3e57fbaa27d0fca8182b502a237f1794b51e491eaf`  
		Last Modified: Tue, 23 Nov 2021 01:22:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8f625347e49af87560b5503ce4cbe1f2b742c43e8ea07dcb0b32452f0aef2`  
		Last Modified: Thu, 02 Dec 2021 20:35:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f58ca42bf8632a09f4cb77c525516e4f2a1fb7ff113bbc462a70a339c900b6f`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fb13589da407a458f7a67290bba0136349e0816c8bf910fd2fe26f0f45720`  
		Last Modified: Thu, 02 Dec 2021 20:38:13 GMT  
		Size: 134.3 MB (134278364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f506237e45790a885a47c45fd9b86175d3b3fe522499bca246f31db841fa3`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4`

```console
$ docker pull julia@sha256:af1ab40b5e90de0a0624d6c728059e24864e6a8477f14f5f980efaf2ea5a2bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.6.4` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4` - linux; arm variant v7

```console
$ docker pull julia@sha256:41e985be7812b17b0f4d3a56c1e3e4c222b095604cdeb963dac28eec963f7148
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141695789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfeac8808213d9adbd26ef9c7717f85bd0e09a33c9ae6753054411f52cf9c7e`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 15:54:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 15:54:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 15:54:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 15:56:52 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 15:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 15:57:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba63f25775a4379e7a82358784a81f364a27c1fbd66d62920077fe305269f65`  
		Last Modified: Thu, 02 Dec 2021 16:02:43 GMT  
		Size: 2.2 MB (2227515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f80d5905455bc4087e33d9e3b560522a954e582437d0e20b06768773d0c1a4`  
		Last Modified: Thu, 02 Dec 2021 16:07:06 GMT  
		Size: 112.9 MB (112895082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4` - linux; 386

```console
$ docker pull julia@sha256:1c24c1394ba495236f0d8dfe723cf64827b13a316b2305d1d9697f9eca652459
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154239864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44a5cd5485bc2f27fc41f13c0d97004af292f4da76776b7543fe62d777d8728`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:20:28 GMT
ENV JULIA_VERSION=1.6.4
# Fri, 03 Dec 2021 11:58:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.4-linux-x86_64.tar.gz'; 			sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.4-linux-armv7l.tar.gz'; 			sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.4-linux-aarch64.tar.gz'; 			sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.4-linux-i686.tar.gz'; 			sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:58:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7823bdf5cf6b356fe4872c3aa19ec265a27cd8fc8cfae3fe886748a7cb422c8`  
		Last Modified: Fri, 03 Dec 2021 12:01:34 GMT  
		Size: 119.3 MB (119329476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:e31f82ce278fcc6285fce308fcb27f0ce5608c206fb552f2ff9bdc462884ede1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318892430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f30e0ce66728515a9abad756ed5b4d101a0cf27ebd98e2205ead99e4f21377`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:15:15 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:23:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:23:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353751959e1e07e0824a3e57fbaa27d0fca8182b502a237f1794b51e491eaf`  
		Last Modified: Tue, 23 Nov 2021 01:22:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8f625347e49af87560b5503ce4cbe1f2b742c43e8ea07dcb0b32452f0aef2`  
		Last Modified: Thu, 02 Dec 2021 20:35:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f58ca42bf8632a09f4cb77c525516e4f2a1fb7ff113bbc462a70a339c900b6f`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fb13589da407a458f7a67290bba0136349e0816c8bf910fd2fe26f0f45720`  
		Last Modified: Thu, 02 Dec 2021 20:38:13 GMT  
		Size: 134.3 MB (134278364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f506237e45790a885a47c45fd9b86175d3b3fe522499bca246f31db841fa3`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:7f36857f78e873e0487424cafa6404bd9009bf38de7470148cee97e52708c3fe
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840183654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e337791a90f19f1bdb55d17453b539366760d77ab304e50d42bb5dc69dcd322`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:16:57 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:23:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:23:51 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:25:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb41f4249d9110eae98c897d297b7ae5d9988bd70dabb4157834c6a4c831907`  
		Last Modified: Tue, 23 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2084c07ff3b28baf268b3d8a1ebdbbe165abfa7557b5c7c226eacabc29c1cf57`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f16be292122f56fd1c53e7510ff183edbad6c65758d300350c3851299ab15c`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94b44743ed005bb9430b0f2b89bc2094fcc5c8516d9921b0a417a9719505f3`  
		Last Modified: Thu, 02 Dec 2021 20:40:50 GMT  
		Size: 134.1 MB (134055514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8c1484f5aa43fa4cb9c4a62c541d048b63be8cc958b2c4b61d412feb2b3470`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:0493a28099b79eae4c9ad622afa014a6d19f6599af08bcc70964bdee33ed2fc1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6407126107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689a1e5c1e173b847ee7fae035c8f1766de55b2c621cc9fe9976a91e34bde733`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:19:24 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:26:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:26:18 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:28:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567970bba379bc9d0742b8793b03e90ffa89398328348fbecd4190381c348917`  
		Last Modified: Tue, 23 Nov 2021 01:24:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104d6d41e17afac4422e3e2be3e6957ecb5bed454bd552176673c7b5e90504a`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee1642c2dc852454e8048e6a6efc9a3820c686d0b799c932b4abad59e69fb6`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e665ccea7290062b33ad896ba3b86ab64ca3bde1aa5d570e04d5c0a96912b77e`  
		Last Modified: Thu, 02 Dec 2021 20:41:30 GMT  
		Size: 134.0 MB (134028484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42054a0452ef38dc7117a8c502f3117ab8c0a00ab6b183aeff5d947bf35ba94`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-alpine`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.4-alpine` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-alpine3.14`

```console
$ docker pull julia@sha256:72db22e0f6ee8dd6bf15f47d6d9102978a39b82a5213a88d74e8ab5ddd58e559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.4-alpine3.14` - linux; amd64

```console
$ docker pull julia@sha256:7bd37afd83771132a076c628443e911613188fd38ed69730e83ad29ac3405f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123721967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88e667c7049e11b615b66bb6fa709f2216d2d03c0518ad9b7dbf12d04d2247`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 13 Nov 2021 06:02:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:02:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 23 Nov 2021 01:26:57 GMT
ENV JULIA_VERSION=1.6.4
# Tue, 23 Nov 2021 01:27:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 23 Nov 2021 01:27:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2f4ada6a836ddc6aad395d8b5de36bd7772c412b43bf6fa5f6f8ab4104b1cc`  
		Last Modified: Tue, 23 Nov 2021 01:29:22 GMT  
		Size: 120.9 MB (120898986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-alpine3.15`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.4-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-bullseye`

```console
$ docker pull julia@sha256:4cb8cd7d4062e7be1f2579bf200b27333b4225a1d2eb2ad85883217e45e3bf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6.4-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:41e985be7812b17b0f4d3a56c1e3e4c222b095604cdeb963dac28eec963f7148
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141695789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfeac8808213d9adbd26ef9c7717f85bd0e09a33c9ae6753054411f52cf9c7e`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 09:05:17 GMT
ADD file:97ce5af9ff4fb4002733d5c402ddc01a13e765d31b85bb6525a7fa797b698e10 in / 
# Thu, 02 Dec 2021 09:05:17 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:54:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 15:54:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 15:54:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 15:54:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 15:56:52 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 15:57:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 15:57:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ba82a1312e1efdcd1cc6eb31cd40358dcec180da31779dac399cba31bf3dc206`  
		Last Modified: Thu, 02 Dec 2021 09:21:03 GMT  
		Size: 26.6 MB (26573192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba63f25775a4379e7a82358784a81f364a27c1fbd66d62920077fe305269f65`  
		Last Modified: Thu, 02 Dec 2021 16:02:43 GMT  
		Size: 2.2 MB (2227515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f80d5905455bc4087e33d9e3b560522a954e582437d0e20b06768773d0c1a4`  
		Last Modified: Thu, 02 Dec 2021 16:07:06 GMT  
		Size: 112.9 MB (112895082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-bullseye` - linux; 386

```console
$ docker pull julia@sha256:1c24c1394ba495236f0d8dfe723cf64827b13a316b2305d1d9697f9eca652459
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.2 MB (154239864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c44a5cd5485bc2f27fc41f13c0d97004af292f4da76776b7543fe62d777d8728`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:20:28 GMT
ENV JULIA_VERSION=1.6.4
# Fri, 03 Dec 2021 11:58:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.4-linux-x86_64.tar.gz'; 			sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.4-linux-armv7l.tar.gz'; 			sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.4-linux-aarch64.tar.gz'; 			sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.4-linux-i686.tar.gz'; 			sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:58:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7823bdf5cf6b356fe4872c3aa19ec265a27cd8fc8cfae3fe886748a7cb422c8`  
		Last Modified: Fri, 03 Dec 2021 12:01:34 GMT  
		Size: 119.3 MB (119329476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-buster`

```console
$ docker pull julia@sha256:b932e93045fcbcebc4181654f3f6d641839d2c95c0158d5616b6e3fbb4bcd957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6.4-buster` - linux; amd64

```console
$ docker pull julia@sha256:48937060ff93ae448b072263d61ee808be1594185bbaa9fadced6db42be29bb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153286261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707777fd72fc7c14d1d3a6935c33af074d56a91f2da13e6593a82cf6a0a9d6fc`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:53 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:44:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:44:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20759da86ee815c76ac66ee463388da4394f7392c03224943a2bd16dc7465c61`  
		Last Modified: Thu, 02 Dec 2021 09:46:46 GMT  
		Size: 4.5 MB (4458542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e35e44e68ba9806eebf32f56ea1f3330676ef3c8e13e26b494a91936e4979`  
		Last Modified: Thu, 02 Dec 2021 09:48:30 GMT  
		Size: 121.7 MB (121673990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:2d765975c8a4cfa884b10d2ba0a9ce8b215d11a4fba8b85c821a8a5c60a2aba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139468568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e00876aecfc2bd801918c448805ee9b2675b8b75222c10ca490c908c5c3706`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 09:06:21 GMT
ADD file:7b30d743b30e84b21888f23cb7f266caba09db98b7a4c8800abebcf03d28c01d in / 
# Thu, 02 Dec 2021 09:06:22 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:55:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 15:55:52 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 15:55:52 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 15:55:53 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 15:58:07 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 15:58:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 15:58:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2aa85085c98821a25a3058f7fc2c6427064f2228ea8eac904e9e7db4dbdaa01a`  
		Last Modified: Thu, 02 Dec 2021 09:22:26 GMT  
		Size: 22.8 MB (22754365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135ada6a5e8fe302e1e9ef466d0da0cc87d2339e25533cb08a044bd660165fa6`  
		Last Modified: Thu, 02 Dec 2021 16:04:23 GMT  
		Size: 3.8 MB (3806048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661f743504ec29bd6b040e2203b21eccc28169a65d7ce2e943132a00df724a7d`  
		Last Modified: Thu, 02 Dec 2021 16:08:39 GMT  
		Size: 112.9 MB (112908155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d9bdb79d807b1654c98525102b535d4d0b94804df9d95143b2d6cd928edf9816
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145549008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba06cb918bf1e3309fb0182c522a5a2fcd6484af3fa337a83bbbb759a6b9b0b7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:44 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:22:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613768401ba4c98b7337eb641463cbd04d29d049c55cf47a4a732e5d16c6aa37`  
		Last Modified: Thu, 02 Dec 2021 10:24:14 GMT  
		Size: 4.3 MB (4338201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b2bba91454eb6c5b227df7159f1129ae22ba1e4c93bf637397e8e08773260`  
		Last Modified: Thu, 02 Dec 2021 10:25:41 GMT  
		Size: 115.3 MB (115287663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-buster` - linux; 386

```console
$ docker pull julia@sha256:856061600bc6474418865589e5254ab378ba945628030b83ea4828d1fdae2a97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.7 MB (151748633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8726472cb16289c1e43d37ec17eed80e849dbc26ceac3260460092e183f471ec`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:20:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:21:02 GMT
ENV JULIA_VERSION=1.6.4
# Fri, 03 Dec 2021 11:58:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.4-linux-x86_64.tar.gz'; 			sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.4-linux-armv7l.tar.gz'; 			sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.4-linux-aarch64.tar.gz'; 			sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.4-linux-i686.tar.gz'; 			sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:58:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c1c092d2a055f47d0a8f69b9a68445f7be8dd96e7cb88a4987b4594b06e10`  
		Last Modified: Thu, 02 Dec 2021 09:24:11 GMT  
		Size: 4.6 MB (4610923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9106b7ba6db81bd4f3eb2549efc07d0c60d3c692318685991e5e31e7021f9d`  
		Last Modified: Fri, 03 Dec 2021 12:02:17 GMT  
		Size: 119.3 MB (119333148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-windowsservercore`

```console
$ docker pull julia@sha256:4ab0a749878e8689f2922f74cf40862a340611eddfdd35d21c7a2c6fdff1ff78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.6.4-windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:e31f82ce278fcc6285fce308fcb27f0ce5608c206fb552f2ff9bdc462884ede1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318892430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f30e0ce66728515a9abad756ed5b4d101a0cf27ebd98e2205ead99e4f21377`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:15:15 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:23:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:23:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353751959e1e07e0824a3e57fbaa27d0fca8182b502a237f1794b51e491eaf`  
		Last Modified: Tue, 23 Nov 2021 01:22:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8f625347e49af87560b5503ce4cbe1f2b742c43e8ea07dcb0b32452f0aef2`  
		Last Modified: Thu, 02 Dec 2021 20:35:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f58ca42bf8632a09f4cb77c525516e4f2a1fb7ff113bbc462a70a339c900b6f`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fb13589da407a458f7a67290bba0136349e0816c8bf910fd2fe26f0f45720`  
		Last Modified: Thu, 02 Dec 2021 20:38:13 GMT  
		Size: 134.3 MB (134278364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f506237e45790a885a47c45fd9b86175d3b3fe522499bca246f31db841fa3`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:7f36857f78e873e0487424cafa6404bd9009bf38de7470148cee97e52708c3fe
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840183654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e337791a90f19f1bdb55d17453b539366760d77ab304e50d42bb5dc69dcd322`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:16:57 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:23:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:23:51 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:25:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb41f4249d9110eae98c897d297b7ae5d9988bd70dabb4157834c6a4c831907`  
		Last Modified: Tue, 23 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2084c07ff3b28baf268b3d8a1ebdbbe165abfa7557b5c7c226eacabc29c1cf57`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f16be292122f56fd1c53e7510ff183edbad6c65758d300350c3851299ab15c`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94b44743ed005bb9430b0f2b89bc2094fcc5c8516d9921b0a417a9719505f3`  
		Last Modified: Thu, 02 Dec 2021 20:40:50 GMT  
		Size: 134.1 MB (134055514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8c1484f5aa43fa4cb9c4a62c541d048b63be8cc958b2c4b61d412feb2b3470`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.4-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:0493a28099b79eae4c9ad622afa014a6d19f6599af08bcc70964bdee33ed2fc1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6407126107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689a1e5c1e173b847ee7fae035c8f1766de55b2c621cc9fe9976a91e34bde733`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:19:24 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:26:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:26:18 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:28:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567970bba379bc9d0742b8793b03e90ffa89398328348fbecd4190381c348917`  
		Last Modified: Tue, 23 Nov 2021 01:24:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104d6d41e17afac4422e3e2be3e6957ecb5bed454bd552176673c7b5e90504a`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee1642c2dc852454e8048e6a6efc9a3820c686d0b799c932b4abad59e69fb6`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e665ccea7290062b33ad896ba3b86ab64ca3bde1aa5d570e04d5c0a96912b77e`  
		Last Modified: Thu, 02 Dec 2021 20:41:30 GMT  
		Size: 134.0 MB (134028484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42054a0452ef38dc7117a8c502f3117ab8c0a00ab6b183aeff5d947bf35ba94`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-windowsservercore-1809`

```console
$ docker pull julia@sha256:9a34215480e787fb91592a090f9539faa35b77399a578423e44b75c8d6d523ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `julia:1.6.4-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:7f36857f78e873e0487424cafa6404bd9009bf38de7470148cee97e52708c3fe
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840183654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e337791a90f19f1bdb55d17453b539366760d77ab304e50d42bb5dc69dcd322`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:16:57 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:23:50 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:23:51 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:25:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:25:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb41f4249d9110eae98c897d297b7ae5d9988bd70dabb4157834c6a4c831907`  
		Last Modified: Tue, 23 Nov 2021 01:23:24 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2084c07ff3b28baf268b3d8a1ebdbbe165abfa7557b5c7c226eacabc29c1cf57`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f16be292122f56fd1c53e7510ff183edbad6c65758d300350c3851299ab15c`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff94b44743ed005bb9430b0f2b89bc2094fcc5c8516d9921b0a417a9719505f3`  
		Last Modified: Thu, 02 Dec 2021 20:40:50 GMT  
		Size: 134.1 MB (134055514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8c1484f5aa43fa4cb9c4a62c541d048b63be8cc958b2c4b61d412feb2b3470`  
		Last Modified: Thu, 02 Dec 2021 20:38:22 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:0b4c54b82e6bfa89d3bbc41a07bf6bc31858bed9915ff75fe1998b605477efef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:1.6.4-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:0493a28099b79eae4c9ad622afa014a6d19f6599af08bcc70964bdee33ed2fc1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6407126107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689a1e5c1e173b847ee7fae035c8f1766de55b2c621cc9fe9976a91e34bde733`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:19:24 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:26:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:26:18 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:28:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:28:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567970bba379bc9d0742b8793b03e90ffa89398328348fbecd4190381c348917`  
		Last Modified: Tue, 23 Nov 2021 01:24:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d104d6d41e17afac4422e3e2be3e6957ecb5bed454bd552176673c7b5e90504a`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ee1642c2dc852454e8048e6a6efc9a3820c686d0b799c932b4abad59e69fb6`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e665ccea7290062b33ad896ba3b86ab64ca3bde1aa5d570e04d5c0a96912b77e`  
		Last Modified: Thu, 02 Dec 2021 20:41:30 GMT  
		Size: 134.0 MB (134028484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42054a0452ef38dc7117a8c502f3117ab8c0a00ab6b183aeff5d947bf35ba94`  
		Last Modified: Thu, 02 Dec 2021 20:41:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.4-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:c4554404ef73bd92d07269b857ce44bffeaf775a45541becaeb2a1bb82bf91e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `julia:1.6.4-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:e31f82ce278fcc6285fce308fcb27f0ce5608c206fb552f2ff9bdc462884ede1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318892430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f30e0ce66728515a9abad756ed5b4d101a0cf27ebd98e2205ead99e4f21377`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 23 Nov 2021 01:15:15 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.4-win64.exe
# Thu, 02 Dec 2021 20:22:08 GMT
ENV JULIA_SHA256=c9b6ecdad4feb57e5af12c9ef1a74993a96edbf87a4dc521d57e338397cee9b2
# Thu, 02 Dec 2021 20:23:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:23:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93353751959e1e07e0824a3e57fbaa27d0fca8182b502a237f1794b51e491eaf`  
		Last Modified: Tue, 23 Nov 2021 01:22:43 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad8f625347e49af87560b5503ce4cbe1f2b742c43e8ea07dcb0b32452f0aef2`  
		Last Modified: Thu, 02 Dec 2021 20:35:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f58ca42bf8632a09f4cb77c525516e4f2a1fb7ff113bbc462a70a339c900b6f`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4fb13589da407a458f7a67290bba0136349e0816c8bf910fd2fe26f0f45720`  
		Last Modified: Thu, 02 Dec 2021 20:38:13 GMT  
		Size: 134.3 MB (134278364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f506237e45790a885a47c45fd9b86175d3b3fe522499bca246f31db841fa3`  
		Last Modified: Thu, 02 Dec 2021 20:35:47 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7`

```console
$ docker pull julia@sha256:844b7fe0bad9693c1100e3a00bd15458a6d24a013f839fc055dc7ed97c78313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.7` - linux; amd64

```console
$ docker pull julia@sha256:3ca9e3ea9f22e94a7ab5810c34d886dfd0b36d46bbe6d2fd9f40b9dede969ebd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166496445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbe8e731d2fa79a2dd2ba509262513645d9d46414cf80d9fc731d5365c8d540`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 09:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:42:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864517c40aa45ba67b0ddab14c8790615497518b12c22292a4346864c8e3049`  
		Last Modified: Thu, 02 Dec 2021 09:46:28 GMT  
		Size: 132.7 MB (132700584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:62b266963dae4f8511229592e819f0a9b67c0a4420eff12664f54169222e2f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158051073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb600b868d0cf978370b597a69953d5e322a267aa4901b7306bc083d046c406`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:20:19 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 10:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:20:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7532ced1e7e4b371c851dd1747b0219196a423ee3c1f7a10d941001204d65c93`  
		Last Modified: Thu, 02 Dec 2021 10:23:57 GMT  
		Size: 125.8 MB (125785808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-alpine`

```console
$ docker pull julia@sha256:99dd839672c220232b4dcc26367d36b0c3ad64c04de47c5d2beee1efbedb593f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.7-alpine` - linux; amd64

```console
$ docker pull julia@sha256:c4c6d620eb0ee01077539aecf2567a60bdb899dd5c91283a994d8ce3311e0baf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134567327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd74482392f4b401c678fa4832ab28c052b7bed345ca4dea6ee78c9f893d8349`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:25:13 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Wed, 01 Dec 2021 02:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='68dc3d7b17fbcceea383b48d82c63c36b899e05f5cd7537a730d7578f65c40ea' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:25:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d7e501fae76372d69280e68cec0a425a50af98a05836156a6db0052fdef49`  
		Last Modified: Wed, 01 Dec 2021 02:28:40 GMT  
		Size: 131.7 MB (131748914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-alpine3.14`

```console
$ docker pull julia@sha256:afac2317bbac87afa0e178b562090863170b30688f4e32b103b85cd4fb175747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.7-alpine3.14` - linux; amd64

```console
$ docker pull julia@sha256:6d4f335ae6e9e46078766392944a136d150073b4e2bff2838a898150980e0a48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134571699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3920170d174db5652d55e60938bebc6cf5289483a374ebf65c0cafe502e1e0e`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 13 Nov 2021 06:02:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:02:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 17 Nov 2021 01:26:53 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Wed, 17 Nov 2021 01:27:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='68dc3d7b17fbcceea383b48d82c63c36b899e05f5cd7537a730d7578f65c40ea' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 17 Nov 2021 01:27:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf5aabbfc0f17d83149f5da4e34cda22bb8c55da971a7dbe3c6fdf331731952`  
		Last Modified: Wed, 17 Nov 2021 01:28:58 GMT  
		Size: 131.7 MB (131748718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-alpine3.15`

```console
$ docker pull julia@sha256:99dd839672c220232b4dcc26367d36b0c3ad64c04de47c5d2beee1efbedb593f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.7-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:c4c6d620eb0ee01077539aecf2567a60bdb899dd5c91283a994d8ce3311e0baf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134567327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd74482392f4b401c678fa4832ab28c052b7bed345ca4dea6ee78c9f893d8349`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:25:13 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Wed, 01 Dec 2021 02:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='68dc3d7b17fbcceea383b48d82c63c36b899e05f5cd7537a730d7578f65c40ea' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:25:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d7e501fae76372d69280e68cec0a425a50af98a05836156a6db0052fdef49`  
		Last Modified: Wed, 01 Dec 2021 02:28:40 GMT  
		Size: 131.7 MB (131748914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-bullseye`

```console
$ docker pull julia@sha256:f8d0cafc97bf9e02f842de9da348c3cb27cd10185c47e87226d3b35e18b2c8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:3ca9e3ea9f22e94a7ab5810c34d886dfd0b36d46bbe6d2fd9f40b9dede969ebd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166496445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbe8e731d2fa79a2dd2ba509262513645d9d46414cf80d9fc731d5365c8d540`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 09:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:42:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864517c40aa45ba67b0ddab14c8790615497518b12c22292a4346864c8e3049`  
		Last Modified: Thu, 02 Dec 2021 09:46:28 GMT  
		Size: 132.7 MB (132700584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:62b266963dae4f8511229592e819f0a9b67c0a4420eff12664f54169222e2f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158051073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb600b868d0cf978370b597a69953d5e322a267aa4901b7306bc083d046c406`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:20:19 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 10:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:20:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7532ced1e7e4b371c851dd1747b0219196a423ee3c1f7a10d941001204d65c93`  
		Last Modified: Thu, 02 Dec 2021 10:23:57 GMT  
		Size: 125.8 MB (125785808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-buster`

```console
$ docker pull julia@sha256:e170ebc1bf0e3ada6cb1c77ee5390016a03ba7c7d7fbefdac292b65e639a737f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.7-buster` - linux; amd64

```console
$ docker pull julia@sha256:138f380c0a8cd869f27839d3d2726e818431ad244d2345ccc5cb861d6e3c2eff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164301507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a759231407880614dc6503bd9071987cffaf3ebf8116d0de57d626917e17`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 09:43:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20759da86ee815c76ac66ee463388da4394f7392c03224943a2bd16dc7465c61`  
		Last Modified: Thu, 02 Dec 2021 09:46:46 GMT  
		Size: 4.5 MB (4458542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b780a5eef27c9124f6c9cc0de170058e377be08beb553e5818b150bfc37ca8`  
		Last Modified: Thu, 02 Dec 2021 09:47:11 GMT  
		Size: 132.7 MB (132689236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:92233267790d005b4cece87aae78b090b0dfa81f37b3705ed9d12d809cd1660b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156040383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcae7bc08563430ec84663f306f7f3aefe81157056f04135b67792f80ee86e8`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:20:57 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 10:21:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613768401ba4c98b7337eb641463cbd04d29d049c55cf47a4a732e5d16c6aa37`  
		Last Modified: Thu, 02 Dec 2021 10:24:14 GMT  
		Size: 4.3 MB (4338201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd76e1bf09bcb1e596c7123ce9c6e59933a7fad861a024ece3b7d35fb8b20dca`  
		Last Modified: Thu, 02 Dec 2021 10:24:33 GMT  
		Size: 125.8 MB (125779038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7-buster` - linux; 386

```console
$ docker pull julia@sha256:6bc17f6e123e101929161a8e67d663644969aabd0248224949638ad252200a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161067535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fb7fe2bf06607e7cbf03841302b886b4e49515b81cd3dcb86642638a17db49`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:20:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:57:22 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c1c092d2a055f47d0a8f69b9a68445f7be8dd96e7cb88a4987b4594b06e10`  
		Last Modified: Thu, 02 Dec 2021 09:24:11 GMT  
		Size: 4.6 MB (4610923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449dabd2d773251d9f33948c89c9e48edf3d7b67efbf2531f849bfbabd8c5676`  
		Last Modified: Fri, 03 Dec 2021 12:00:52 GMT  
		Size: 128.7 MB (128652050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-windowsservercore`

```console
$ docker pull julia@sha256:ddc566b528620adc3b6c879091d20577ef2884a92f70e18f7f09249d9005bd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.7-windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:0610b340222e87e165f1ef09d5d94552f085371a0ce548b8954fd2bb2ead3cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `julia:1.7-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:10e088aad15e9619bbf141e37f769c15a2d799c98156d71ea47aef15072617c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:1.7-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:65bdc4b753a26cdc05f71ea5c9e792a8bdbe771da35eee7fb96c58ef5b90f0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `julia:1.7-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0`

```console
$ docker pull julia@sha256:844b7fe0bad9693c1100e3a00bd15458a6d24a013f839fc055dc7ed97c78313e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.7.0` - linux; amd64

```console
$ docker pull julia@sha256:3ca9e3ea9f22e94a7ab5810c34d886dfd0b36d46bbe6d2fd9f40b9dede969ebd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166496445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbe8e731d2fa79a2dd2ba509262513645d9d46414cf80d9fc731d5365c8d540`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 09:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:42:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864517c40aa45ba67b0ddab14c8790615497518b12c22292a4346864c8e3049`  
		Last Modified: Thu, 02 Dec 2021 09:46:28 GMT  
		Size: 132.7 MB (132700584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:62b266963dae4f8511229592e819f0a9b67c0a4420eff12664f54169222e2f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158051073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb600b868d0cf978370b597a69953d5e322a267aa4901b7306bc083d046c406`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:20:19 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 10:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:20:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7532ced1e7e4b371c851dd1747b0219196a423ee3c1f7a10d941001204d65c93`  
		Last Modified: Thu, 02 Dec 2021 10:23:57 GMT  
		Size: 125.8 MB (125785808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-alpine`

```console
$ docker pull julia@sha256:99dd839672c220232b4dcc26367d36b0c3ad64c04de47c5d2beee1efbedb593f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.7.0-alpine` - linux; amd64

```console
$ docker pull julia@sha256:c4c6d620eb0ee01077539aecf2567a60bdb899dd5c91283a994d8ce3311e0baf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134567327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd74482392f4b401c678fa4832ab28c052b7bed345ca4dea6ee78c9f893d8349`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:25:13 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Wed, 01 Dec 2021 02:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='68dc3d7b17fbcceea383b48d82c63c36b899e05f5cd7537a730d7578f65c40ea' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:25:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d7e501fae76372d69280e68cec0a425a50af98a05836156a6db0052fdef49`  
		Last Modified: Wed, 01 Dec 2021 02:28:40 GMT  
		Size: 131.7 MB (131748914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-alpine3.14`

```console
$ docker pull julia@sha256:afac2317bbac87afa0e178b562090863170b30688f4e32b103b85cd4fb175747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.7.0-alpine3.14` - linux; amd64

```console
$ docker pull julia@sha256:6d4f335ae6e9e46078766392944a136d150073b4e2bff2838a898150980e0a48
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134571699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3920170d174db5652d55e60938bebc6cf5289483a374ebf65c0cafe502e1e0e`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 13 Nov 2021 06:02:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:02:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 17 Nov 2021 01:26:53 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Wed, 17 Nov 2021 01:27:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='68dc3d7b17fbcceea383b48d82c63c36b899e05f5cd7537a730d7578f65c40ea' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 17 Nov 2021 01:27:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf5aabbfc0f17d83149f5da4e34cda22bb8c55da971a7dbe3c6fdf331731952`  
		Last Modified: Wed, 17 Nov 2021 01:28:58 GMT  
		Size: 131.7 MB (131748718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-alpine3.15`

```console
$ docker pull julia@sha256:99dd839672c220232b4dcc26367d36b0c3ad64c04de47c5d2beee1efbedb593f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.7.0-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:c4c6d620eb0ee01077539aecf2567a60bdb899dd5c91283a994d8ce3311e0baf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134567327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd74482392f4b401c678fa4832ab28c052b7bed345ca4dea6ee78c9f893d8349`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:25:13 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Wed, 01 Dec 2021 02:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='68dc3d7b17fbcceea383b48d82c63c36b899e05f5cd7537a730d7578f65c40ea' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:25:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4d7e501fae76372d69280e68cec0a425a50af98a05836156a6db0052fdef49`  
		Last Modified: Wed, 01 Dec 2021 02:28:40 GMT  
		Size: 131.7 MB (131748914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-bullseye`

```console
$ docker pull julia@sha256:f8d0cafc97bf9e02f842de9da348c3cb27cd10185c47e87226d3b35e18b2c8b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.7.0-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:3ca9e3ea9f22e94a7ab5810c34d886dfd0b36d46bbe6d2fd9f40b9dede969ebd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166496445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbe8e731d2fa79a2dd2ba509262513645d9d46414cf80d9fc731d5365c8d540`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 09:42:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:42:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864517c40aa45ba67b0ddab14c8790615497518b12c22292a4346864c8e3049`  
		Last Modified: Thu, 02 Dec 2021 09:46:28 GMT  
		Size: 132.7 MB (132700584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:62b266963dae4f8511229592e819f0a9b67c0a4420eff12664f54169222e2f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158051073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb600b868d0cf978370b597a69953d5e322a267aa4901b7306bc083d046c406`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:20:19 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 10:20:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:20:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7532ced1e7e4b371c851dd1747b0219196a423ee3c1f7a10d941001204d65c93`  
		Last Modified: Thu, 02 Dec 2021 10:23:57 GMT  
		Size: 125.8 MB (125785808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-buster`

```console
$ docker pull julia@sha256:e170ebc1bf0e3ada6cb1c77ee5390016a03ba7c7d7fbefdac292b65e639a737f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.7.0-buster` - linux; amd64

```console
$ docker pull julia@sha256:138f380c0a8cd869f27839d3d2726e818431ad244d2345ccc5cb861d6e3c2eff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164301507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e9a759231407880614dc6503bd9071987cffaf3ebf8116d0de57d626917e17`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 09:43:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20759da86ee815c76ac66ee463388da4394f7392c03224943a2bd16dc7465c61`  
		Last Modified: Thu, 02 Dec 2021 09:46:46 GMT  
		Size: 4.5 MB (4458542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b780a5eef27c9124f6c9cc0de170058e377be08beb553e5818b150bfc37ca8`  
		Last Modified: Thu, 02 Dec 2021 09:47:11 GMT  
		Size: 132.7 MB (132689236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:92233267790d005b4cece87aae78b090b0dfa81f37b3705ed9d12d809cd1660b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156040383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fcae7bc08563430ec84663f306f7f3aefe81157056f04135b67792f80ee86e8`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:20:57 GMT
ENV JULIA_VERSION=1.7.0-rc3
# Thu, 02 Dec 2021 10:21:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='cbf33c533d6f226161f08cdc3cec16745a3dc5afdfbaece95e3f2a5e0b6b7886' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='fff9370f58fd8f94f12a14d38c32d25b9e493d62a6d992edfc378caf9ef8d1cc' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0662f9f31c87559ec33a24b3b83df85071357708287678ca78c7fa4498d05e5c' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9ee7692faee05d7dbe431c59850542d95d260368bbf6d4f0ccdd03be07fef817' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613768401ba4c98b7337eb641463cbd04d29d049c55cf47a4a732e5d16c6aa37`  
		Last Modified: Thu, 02 Dec 2021 10:24:14 GMT  
		Size: 4.3 MB (4338201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd76e1bf09bcb1e596c7123ce9c6e59933a7fad861a024ece3b7d35fb8b20dca`  
		Last Modified: Thu, 02 Dec 2021 10:24:33 GMT  
		Size: 125.8 MB (125779038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0-buster` - linux; 386

```console
$ docker pull julia@sha256:6bc17f6e123e101929161a8e67d663644969aabd0248224949638ad252200a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161067535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fb7fe2bf06607e7cbf03841302b886b4e49515b81cd3dcb86642638a17db49`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:20:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:57:22 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c1c092d2a055f47d0a8f69b9a68445f7be8dd96e7cb88a4987b4594b06e10`  
		Last Modified: Thu, 02 Dec 2021 09:24:11 GMT  
		Size: 4.6 MB (4610923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449dabd2d773251d9f33948c89c9e48edf3d7b67efbf2531f849bfbabd8c5676`  
		Last Modified: Fri, 03 Dec 2021 12:00:52 GMT  
		Size: 128.7 MB (128652050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-windowsservercore`

```console
$ docker pull julia@sha256:ddc566b528620adc3b6c879091d20577ef2884a92f70e18f7f09249d9005bd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:1.7.0-windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0-windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.7.0-windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-windowsservercore-1809`

```console
$ docker pull julia@sha256:0610b340222e87e165f1ef09d5d94552f085371a0ce548b8954fd2bb2ead3cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `julia:1.7.0-windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:10e088aad15e9619bbf141e37f769c15a2d799c98156d71ea47aef15072617c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:1.7.0-windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.7.0-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:65bdc4b753a26cdc05f71ea5c9e792a8bdbe771da35eee7fb96c58ef5b90f0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `julia:1.7.0-windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine3.14`

```console
$ docker pull julia@sha256:72db22e0f6ee8dd6bf15f47d6d9102978a39b82a5213a88d74e8ab5ddd58e559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.14` - linux; amd64

```console
$ docker pull julia@sha256:7bd37afd83771132a076c628443e911613188fd38ed69730e83ad29ac3405f8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123721967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88e667c7049e11b615b66bb6fa709f2216d2d03c0518ad9b7dbf12d04d2247`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Sat, 13 Nov 2021 06:02:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Nov 2021 06:02:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 23 Nov 2021 01:26:57 GMT
ENV JULIA_VERSION=1.6.4
# Tue, 23 Nov 2021 01:27:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Tue, 23 Nov 2021 01:27:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2f4ada6a836ddc6aad395d8b5de36bd7772c412b43bf6fa5f6f8ab4104b1cc`  
		Last Modified: Tue, 23 Nov 2021 01:29:22 GMT  
		Size: 120.9 MB (120898986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine3.15`

```console
$ docker pull julia@sha256:10a717a11632595a3bbe626506028061d788fc08ff3356196dd261c565c67bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:12794c6477afa1b1a401867341d1318b5db4268c52f9458e2e704b8d88c5cc84
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123717269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2fa1d4478a6131de1bcfb5e9a863d6dc6e3ab6e1790725948ea1706d9af30`
-	Default Command: `["julia"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 01 Dec 2021 02:25:12 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Dec 2021 02:25:12 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 01 Dec 2021 02:26:08 GMT
ENV JULIA_VERSION=1.6.4
# Wed, 01 Dec 2021 02:26:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) tarArch='x86_64'; dirArch='x64'; sha256='63f121dffa982ff9b53c7c8a334830e17e2c9d2efa79316a548d29f7f8925e66' ;; 		*) echo >&2 "error: current architecture ($apkArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	wget -O julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz.asc"; 	wget -O julia.tar.gz     "https://julialang-s3.julialang.org/bin/musl/${dirArch}/${folder}/julia-${JULIA_VERSION}-musl-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Wed, 01 Dec 2021 02:26:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae90df759d355407b8f983dd26a75acbf89982a56883f52f751813444a765336`  
		Last Modified: Wed, 01 Dec 2021 02:30:01 GMT  
		Size: 120.9 MB (120898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bullseye`

```console
$ docker pull julia@sha256:d71c37dc6cdfa071d88b2680feb47cf922f26d668a372162bf7ef11d211b1052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:buster`

```console
$ docker pull julia@sha256:87116c86344cf4ab009df1411b870b2024d3445302c61d54b4555a68806f3f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:48937060ff93ae448b072263d61ee808be1594185bbaa9fadced6db42be29bb8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153286261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707777fd72fc7c14d1d3a6935c33af074d56a91f2da13e6593a82cf6a0a9d6fc`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:43 GMT
ADD file:70f893355b4ecf317b289874ea624aa52c30735086e26de45bad73f57d16757b in / 
# Thu, 02 Dec 2021 02:48:43 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:56 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:56 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:53 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:44:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:44:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ffbb094f4f9e7c61d97c2b409f3e8154e2621a5074a0087d35f1849e665d0d34`  
		Last Modified: Thu, 02 Dec 2021 02:54:33 GMT  
		Size: 27.2 MB (27153729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20759da86ee815c76ac66ee463388da4394f7392c03224943a2bd16dc7465c61`  
		Last Modified: Thu, 02 Dec 2021 09:46:46 GMT  
		Size: 4.5 MB (4458542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0e35e44e68ba9806eebf32f56ea1f3330676ef3c8e13e26b494a91936e4979`  
		Last Modified: Thu, 02 Dec 2021 09:48:30 GMT  
		Size: 121.7 MB (121673990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d9bdb79d807b1654c98525102b535d4d0b94804df9d95143b2d6cd928edf9816
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145549008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba06cb918bf1e3309fb0182c522a5a2fcd6484af3fa337a83bbbb759a6b9b0b7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:34 GMT
ADD file:83d9e760a84be2bd8754e31e33b3f782b44f6e7b7e02c156f519715c88c40615 in / 
# Thu, 02 Dec 2021 08:08:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:44 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:22:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2a37a2e6ba8cbf21e3950cf7b2455f0af054667b6a35719fb2bd6070973bfa76`  
		Last Modified: Thu, 02 Dec 2021 08:41:37 GMT  
		Size: 25.9 MB (25923144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613768401ba4c98b7337eb641463cbd04d29d049c55cf47a4a732e5d16c6aa37`  
		Last Modified: Thu, 02 Dec 2021 10:24:14 GMT  
		Size: 4.3 MB (4338201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39b2bba91454eb6c5b227df7159f1129ae22ba1e4c93bf637397e8e08773260`  
		Last Modified: Thu, 02 Dec 2021 10:25:41 GMT  
		Size: 115.3 MB (115287663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:6bc17f6e123e101929161a8e67d663644969aabd0248224949638ad252200a34
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161067535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fb7fe2bf06607e7cbf03841302b886b4e49515b81cd3dcb86642638a17db49`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:40:25 GMT
ADD file:9063906ecf2b5c82bf37cb574e78f61add2cd7aa8d0675647be379e30e19b6a9 in / 
# Thu, 02 Dec 2021 02:40:25 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:59 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:59 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:20:00 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:57:22 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b938b4b72623e9d1494d498630cd883df97fd6882fb9e0edb7af6714fce4e83`  
		Last Modified: Thu, 02 Dec 2021 02:49:02 GMT  
		Size: 27.8 MB (27804562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610c1c092d2a055f47d0a8f69b9a68445f7be8dd96e7cb88a4987b4594b06e10`  
		Last Modified: Thu, 02 Dec 2021 09:24:11 GMT  
		Size: 4.6 MB (4610923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449dabd2d773251d9f33948c89c9e48edf3d7b67efbf2531f849bfbabd8c5676`  
		Last Modified: Fri, 03 Dec 2021 12:00:52 GMT  
		Size: 128.7 MB (128652050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:latest`

```console
$ docker pull julia@sha256:6813817da8dd4de68259d62eb0a685c351353a69de15c02d631305b13d7fb09a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:7a57877428af4f89aeadff7c471c73f3930f353febe4303c9817a54a0ad93773
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82f237302a983426375f0aa600b167180f7132b24384c8a67635947632c5eb7`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:48:20 GMT
ADD file:ece5ff85ca549f0b1e9139d29dcb43a52af672d0591c423e28180f6d8d700ad7 in / 
# Thu, 02 Dec 2021 02:48:21 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:42:08 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:42:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:42:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 09:43:28 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 09:43:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 09:43:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e5ae68f740265288a4888db98d2999a638fdcb6d725f427678814538d253aa4d`  
		Last Modified: Thu, 02 Dec 2021 02:53:46 GMT  
		Size: 31.4 MB (31370221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55e18473ecc625d930f2f4852d4fb5fcd720e0f41240db5bee9d0f9b2841d65`  
		Last Modified: Thu, 02 Dec 2021 09:46:07 GMT  
		Size: 2.4 MB (2425640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a91489626fba4b10ff5cada14b5e09bccee3c981c0b944c9b5f505d31758a`  
		Last Modified: Thu, 02 Dec 2021 09:47:55 GMT  
		Size: 121.7 MB (121673787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4333aba468905a5a4eb5592dd3b8818196a26e3dd6b82e6872a65dfd1c89100a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb9fe8f639daee2fb401cf23736bdbb4d854ae697c86d4cbced8903b9f80ba`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 08:08:09 GMT
ADD file:002f2f7c6dc806b24b6c365882acd59d2b3d3fcec46d8fd99130b07a4575c88c in / 
# Thu, 02 Dec 2021 08:08:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 10:20:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 10:20:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 10:20:17 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 10:20:18 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 02 Dec 2021 10:21:19 GMT
ENV JULIA_VERSION=1.6.4
# Thu, 02 Dec 2021 10:21:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='52244ae47697e8073dfbc9d1251b0422f0dbd1fbe1a41da4b9f7ddf0506b2132' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='9ad3f6bd71eb6840d4cef1569855da20c0b4931a2bdf77703a64df672b0702a1' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='072daac7229c15fa41d0c1b65b8a3d6ee747323d02f5943da3846b075291b48b' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='9d43d642174cf22cf0fde18dc2578c84f357d2c619b9d846d3a6da4192ba48cf' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Thu, 02 Dec 2021 10:21:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:968621624b326084ed82349252b333e649eaab39f71866edb2b9a4f847283680`  
		Last Modified: Thu, 02 Dec 2021 08:40:45 GMT  
		Size: 30.1 MB (30056536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b76d02a380e42c7b48c27d8027217d2603a80abfae7351c4cd314f18d101627`  
		Last Modified: Thu, 02 Dec 2021 10:23:37 GMT  
		Size: 2.2 MB (2208729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718513ebf95051a2e77cd6e726c66bc379eec8de4e59bd82b38a614636903583`  
		Last Modified: Thu, 02 Dec 2021 10:25:06 GMT  
		Size: 115.3 MB (115278610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:4c72a8a1b6db0ef4a6ce933e117052d86293b8ac9905ad7d2f2a99876f22c3be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163557907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43cc91979b796bebea43b172a397c1e1d40fd07d35a870db3a729d28e8cbb9c9`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 02 Dec 2021 02:39:54 GMT
ADD file:0284c10b06ba22560408e1e14c1147887f4302c79dba143277ece2e333d6dcbc in / 
# Thu, 02 Dec 2021 02:39:55 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:19:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:19:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 02 Dec 2021 09:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Dec 2021 09:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 03 Dec 2021 11:56:43 GMT
ENV JULIA_VERSION=1.7.0
# Fri, 03 Dec 2021 11:57:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.7/julia-1.7.0-linux-x86_64.tar.gz'; 			sha256='7299f3a638aec5e0b9e14eaf0e6221c4fe27189aa0b38ac5a36f03f0dc4c0d40'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.7/julia-1.7.0-linux-aarch64.tar.gz'; 			sha256='85a93659ef588b7ee9e3eb2ee1e8b1ba8bb200adc4389afed054be44e51e6540'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.7/julia-1.7.0-linux-i686.tar.gz'; 			sha256='e4498be9c2449791093938e8e4f6a93a708d2a8bf27605c835c7409c0a57695d'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 03 Dec 2021 11:57:12 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2df7932f17d752876c686aa22054692a38e88e182dd7b6a5cca7ffce4ffe6f84`  
		Last Modified: Thu, 02 Dec 2021 02:47:59 GMT  
		Size: 32.4 MB (32380814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c26dd9e12ca161e0d08bf5b14bcb1f80a4ae55a052739f8a0eb7cc36628df37`  
		Last Modified: Thu, 02 Dec 2021 09:23:26 GMT  
		Size: 2.5 MB (2529574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410e45fdeb48de4850169468974008b16b4d452c14db5db3cc7ebe4288ef7e50`  
		Last Modified: Fri, 03 Dec 2021 12:00:08 GMT  
		Size: 128.6 MB (128647519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:ddc566b528620adc3b6c879091d20577ef2884a92f70e18f7f09249d9005bd1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.20348.350; amd64
	-	windows version 10.0.17763.2300; amd64
	-	windows version 10.0.14393.4770; amd64

### `julia:windowsservercore` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:0610b340222e87e165f1ef09d5d94552f085371a0ce548b8954fd2bb2ead3cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull julia@sha256:621dee76e2d3a2a49901abbf68256add379b800081014918cdda1e60ef99e337
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2850775507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb807b4feaed4adface87fbfefcaef85e083c3b8f414c90b6ec8c9a277e0a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 04 Nov 2021 00:30:48 GMT
RUN Install update 1809-amd64
# Wed, 10 Nov 2021 01:42:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:16:39 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:16:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:16:41 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:19:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1f4c7287c99b95fce227924349d1d139aceb37d97b555144bd5808935b6eab0`  
		Size: 987.8 MB (987788268 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b35c0957cca5902f3108e43a3c2c11250dc754ee0bb43900eb0719b4350f0bc2`  
		Last Modified: Wed, 10 Nov 2021 02:08:44 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f1951bc10b3f16a122ed76985fa2d38c6302c252c0e53eaa6f97bdb9a564a7`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ba1b5850ed94ca6498046291b133311cfb020b07051333cdb8fe69e27f70ca`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0b97cc61a8838dcd4f1fe4a8e0edac78cc87864d9727c5d0a4ec1ce54f332c`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3029eace430ebf0b5307cdd3f01e3e6e6d251a97efaa85d2a1ff4edb68c8a8`  
		Last Modified: Thu, 02 Dec 2021 20:32:38 GMT  
		Size: 144.6 MB (144647287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc71a9b37ced075b062e7622e4d296742ee50e2b368af35bb97113e518841f`  
		Last Modified: Thu, 02 Dec 2021 20:30:01 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:10e088aad15e9619bbf141e37f769c15a2d799c98156d71ea47aef15072617c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `julia:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull julia@sha256:9bcb4a2900c1453de42963a7f097cf2f3a3126a0cc4afbe3d502fc51842965ce
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6417714013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b505a3305c49ea030e025c63c1d505b5efd780dc483a9ef22aff075ba08e081`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:19:22 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:19:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:19:24 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:21:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:21:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a66ccb2b96c4c0726117d397da2d6f37f565a4f07bb0c477a0ba63e296c4b3`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f20bfc47b18925f0e96c85453e8ff4c52a2cf340ffb9023dbe970a0c27fca34`  
		Last Modified: Thu, 02 Dec 2021 20:32:53 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bcbd398cdaa6f2a121e93bfe7e79d66a534d2737f1fa8af659b1875124a17b`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adedd2b0a0854a65eb0008cb3dd36cbecb00ce04b0e471cea402858c449f99d0`  
		Last Modified: Thu, 02 Dec 2021 20:35:29 GMT  
		Size: 144.6 MB (144616051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a0e864f5c4a1c54874257eaa363443c8cfbdc31a88f3e81cc59f241e4c113`  
		Last Modified: Thu, 02 Dec 2021 20:32:52 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:65bdc4b753a26cdc05f71ea5c9e792a8bdbe771da35eee7fb96c58ef5b90f0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.350; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.350; amd64

```console
$ docker pull julia@sha256:726a2beb56612e2f1395b8ef433ab8a3e25f42ce21e27e5ebfda5d7ea8d6e4d4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2329488307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fd9ebac07ac936dc4182fa3baeec41d36d224aa13d7f1ad62b9bb780424d54`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Wed, 03 Nov 2021 08:36:33 GMT
RUN Install update ltsc2022-amd64
# Wed, 10 Nov 2021 01:38:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 02 Dec 2021 20:14:55 GMT
ENV JULIA_VERSION=1.7.0
# Thu, 02 Dec 2021 20:14:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.0-win64.exe
# Thu, 02 Dec 2021 20:14:58 GMT
ENV JULIA_SHA256=40c6704a9f27031729610e177aa1cae5386336c7fea9c2e021e3b14d230498d5
# Thu, 02 Dec 2021 20:16:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 02 Dec 2021 20:16:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0eb404f1860fa8786ad09d1d9fe9fd580115f83cd38623bc4eb0c46abdaa0a3`  
		Size: 932.9 MB (932907933 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:27ded59d7006d9d7bffa7c253cd04a900a5d6b0d47b84d0edd624d12fd64cdc9`  
		Last Modified: Wed, 10 Nov 2021 02:07:39 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cd7740ea455106167cad571be3d8541827013b93883f429c0bc42cdb52f7ad`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc0b88a1a6da63ae9984ea14dd2e324773503f353b292ebf5eb7232cb625ab5`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25769ef8ad5c07c032eae43bbf08b7d93bde72e256ec6b794ef2c5a4c3e37a88`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05cb0135d1d0beb47663355c8a68859423d200cb07fc52baaaca5097681a028a`  
		Last Modified: Thu, 02 Dec 2021 20:29:45 GMT  
		Size: 144.9 MB (144874229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4fa037d78f69fc11c966bb0543794e752fc7d99790b4bfe829337f07240656`  
		Last Modified: Thu, 02 Dec 2021 20:29:11 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
