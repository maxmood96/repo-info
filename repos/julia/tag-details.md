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
-	[`julia:1.8.2`](#julia182)
-	[`julia:1.8.2-alpine`](#julia182-alpine)
-	[`julia:1.8.2-alpine3.15`](#julia182-alpine315)
-	[`julia:1.8.2-alpine3.16`](#julia182-alpine316)
-	[`julia:1.8.2-bullseye`](#julia182-bullseye)
-	[`julia:1.8.2-buster`](#julia182-buster)
-	[`julia:1.8.2-windowsservercore`](#julia182-windowsservercore)
-	[`julia:1.8.2-windowsservercore-1809`](#julia182-windowsservercore-1809)
-	[`julia:1.8.2-windowsservercore-ltsc2022`](#julia182-windowsservercore-ltsc2022)
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
$ docker pull julia@sha256:31b661ff9b0bacc635afebf74a41061e761091dfa4e0f60e3f5db62b0e748862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine3.15`

```console
$ docker pull julia@sha256:38914c91fdc9be54e8fee495b02ec2c618b398a7715a5019b076237ce7ccc565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:be7a89dfc616b44b83cb9e2e7413ef0296974f541602183a9504eb98c0dfd67f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149958895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c947abb57660db81dd3e216198ef24473b06894a4307c969bbf52619c56afa`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:48:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:48:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7952d73a20c790439007f53998172937cbf1b838ab52ce6411d56fa0cd4d68a`  
		Last Modified: Thu, 06 Oct 2022 22:57:55 GMT  
		Size: 147.1 MB (147135383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-alpine3.16`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bullseye`

```console
$ docker pull julia@sha256:183b4b5727f6996d59374eb4dd8742d12be71b32641bb32c2ef9e3371817731a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-buster`

```console
$ docker pull julia@sha256:449fb68a71c39009c7a157e8c3e112bbf5f18a9c41c39d4ac290fd8cd3f53187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:4fae4331e7e21afda51912a3eaee115723f85a5513fa23aef1ed8b75c53d0062
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177432150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abf5b0b7bbc388655b6555168e61f5c1a7de354aeb23740b8dfb0496c80e8b6`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c2c91b60a243ec7a657c586ba51a4c16b8d24a1d693ebb322bcc1bdfcf1b`  
		Last Modified: Wed, 05 Oct 2022 04:15:58 GMT  
		Size: 4.5 MB (4468448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7762e9536e599b6aafe5001040d2ee204076444131dbc5b69ed1910652e7220`  
		Last Modified: Wed, 05 Oct 2022 04:16:20 GMT  
		Size: 145.8 MB (145825659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1e5f54d0ad4fd36bd1d679e074391447933dc8a127970197083d71c16a8a568a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169894074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f5f6260ec64d1f7c8dcf2342aab66630ea433847a0e919f53868e8c53871e7`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8297636379925d4f7ea1fdac2965d49b5cac0c8b948da968e5bea62d5b0757`  
		Last Modified: Wed, 05 Oct 2022 03:04:23 GMT  
		Size: 139.6 MB (139635231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:37a1da12330b7d038acddfc55e8980f999a87cbada9b43ace6cfb4e28ea2f350
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175134939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dabb27a643c5ceb1f4eedc67f354efa8ba52d127c5450ddcf4931bc1a32518`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:18 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb28420c7c0fd820677e95822c0e1e9da492a9d8a6950338327051151adb5d`  
		Last Modified: Wed, 05 Oct 2022 02:13:06 GMT  
		Size: 142.7 MB (142720561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:5ba56e049b8e09c7a05d0620b12a3121e98ce39ac100b6df6b14e151dde32fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:0891bbcecea522e4e7cb5b7a367b6e00e3a2323d37bd6a48b704d415ae3aea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1d40145cf504997e2e7526e95bd865147d1c11e0ea1e2d3a098aafeaade3fe11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6`

```console
$ docker pull julia@sha256:6be6530120577d69e76c19d7765e8a2a0b92935150423abfada066f676c95958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.6` - linux; amd64

```console
$ docker pull julia@sha256:69fc7255c083cfaea291719eadc3f24d8cc395bb75893638d243605ac1424937
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156486591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634db3704dfd188d5aa7a0f5bfde32f598c561e5394fdfb880f2611d53cb880b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:14:01 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 04:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a229db433d9600f62d1e04fd517749652a5a0fad9b51bc8cf426c5c12d5862`  
		Last Modified: Wed, 05 Oct 2022 04:16:58 GMT  
		Size: 122.6 MB (122639897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; arm variant v7

```console
$ docker pull julia@sha256:dc9cd6d5a597a14a193d495d02bbe2ca60dab2a5fb01563ee27a1c1f6c1ab698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142495823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c69cb56c8673f04379daacda1ad823d719da1eff37bd01ee0f8876d5082e3b4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:57:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:57:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:57:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 05:04:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 05:04:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad2fd8944c2866a23946bb173e0e383044efc6cc17556c88712007d29fbb742`  
		Last Modified: Wed, 05 Oct 2022 05:05:36 GMT  
		Size: 2.2 MB (2228860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38a8a3a11ec4c902839113094aeae003ce8902db81798d38d1b6c5db8f8622`  
		Last Modified: Wed, 05 Oct 2022 05:06:02 GMT  
		Size: 113.7 MB (113687764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4b3d928fb5fc3a6090c038c8ec0400bba3f654ebe99fd184ca1dada4fb302f5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148487307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d18bd6333c8505e700b3e5c9662dd874d29407bc51a3928b4dc300c0e52c096`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:57 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 03:02:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:02:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa0ca1db3a8b43b540209193186012fdcec24454da49b7db9e32304fd1050e2`  
		Last Modified: Wed, 05 Oct 2022 03:04:58 GMT  
		Size: 116.2 MB (116213264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - linux; 386

```console
$ docker pull julia@sha256:eed1e43b274fbd25a321d54d93d1ea23add302e972578319e113c349aa7020fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154813677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790d2c8a134679f481fdf4a79866bd51d0384c7790c84bb5e94ee3137378527f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:45 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 02:11:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:11:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecaaeb59bbf6af29174938b9dc562aafa64c6ea714d9a0bafec2e63468275be`  
		Last Modified: Wed, 05 Oct 2022 02:13:39 GMT  
		Size: 120.1 MB (120090666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:34f0ef538a98f4fceb49284f465d6a02973f403df639dd0f59b16e4835b1b4d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550890943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad32493df8519291d48f606f52bfa0bf7427fc178e352f096ff27ae2d6532b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:06:42 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:06:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:06:44 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:07:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4e0cf35d121019206cf2b70cbd13b415069e0526d66b8139de599cd62583d`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fe6483e5d57d263acfaabb07480e724baa8eb33dff561897286ccc91a8af9`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2565c05345376ffdfa512de2c9201d03ae98a827b49dccb5f3d74b060e2e`  
		Last Modified: Wed, 12 Oct 2022 15:12:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6030bfa6a596b3bd6e1dd58900e61d21995691eff90baf3f170f21261cc27c`  
		Last Modified: Wed, 12 Oct 2022 15:12:58 GMT  
		Size: 134.7 MB (134660486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfc11771396e7dab867c32ba66aa2e14c1fc5ab6c66509cc9e7f074ff249e5`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:6d50044816a3d6c929350dffa15a8bf5ca108f16288ace088a43f68cff1c9941
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2845581797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8c3f74e0120f6ea3b2bd61d80a7e65d88746a9cdbdcfe3b11dd1f9718d9bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:08:14 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:08:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:08:16 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:10:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5521024befbc8e402dfb54dba5a88b96791543090d98bf68992b52259541b`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed136e7af2fef739ea1164a8f3535d71d81d70b2f355f6e2464958fdf1936053`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dd422d2bef6b74e6bfc13cdfb305f46baf9e23c61b413dea44b2dff639d1e`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985cc5fc071101024b8c101fcea4398edc11c3aff42cbec8f1a6d10f7ddc916`  
		Last Modified: Wed, 12 Oct 2022 15:13:38 GMT  
		Size: 134.4 MB (134410742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d6c7151cb560c7cb9bdc9e428c5195f18ed002469b66cf823d09ca174c1f4`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine`

```console
$ docker pull julia@sha256:2589757b00b345796a9d19ae2d006b721016da0eb56891e922eeb0f7067dbbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine` - linux; amd64

```console
$ docker pull julia@sha256:5698ae540981aea211af20caf022be767a8aaf2ab21ca02ba71c6155b0be6247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca6d1c792a16baf4c80e75d5521042da08c49a9d4f16977cd682a8b2ec7014b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:48:18 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 06 Oct 2022 22:55:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:55:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2155182571b34a72eb201caaf6b72c0c4865409b4d31c1adf7bb7a9ad64c3ea0`  
		Last Modified: Thu, 06 Oct 2022 22:58:30 GMT  
		Size: 121.8 MB (121828697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine3.15`

```console
$ docker pull julia@sha256:dabdc633888297b0fff4b09b1e16f0020a89e7a35d123f0e07f76dd22c50c94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:e94cc93368b7ebde8e1ebf8b06ec2da396592b46d9aead799b9ce8b9155c1b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124652062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc78044f85060bcff7a6c4d9e9d40545c87106711bbe9ddbfebed0c9cd32917`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:55:56 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 06 Oct 2022 22:56:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:56:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b56890552fa59b38e90510ee05c9235377bca048c4b6acdf5b6bbf015c17263`  
		Last Modified: Thu, 06 Oct 2022 22:59:05 GMT  
		Size: 121.8 MB (121828550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-alpine3.16`

```console
$ docker pull julia@sha256:2589757b00b345796a9d19ae2d006b721016da0eb56891e922eeb0f7067dbbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:5698ae540981aea211af20caf022be767a8aaf2ab21ca02ba71c6155b0be6247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca6d1c792a16baf4c80e75d5521042da08c49a9d4f16977cd682a8b2ec7014b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:48:18 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 06 Oct 2022 22:55:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:55:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2155182571b34a72eb201caaf6b72c0c4865409b4d31c1adf7bb7a9ad64c3ea0`  
		Last Modified: Thu, 06 Oct 2022 22:58:30 GMT  
		Size: 121.8 MB (121828697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-bullseye`

```console
$ docker pull julia@sha256:2657d5360026d785085a0bd46387540d91281e0f00144b6cc097f290b5c31c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:69fc7255c083cfaea291719eadc3f24d8cc395bb75893638d243605ac1424937
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156486591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634db3704dfd188d5aa7a0f5bfde32f598c561e5394fdfb880f2611d53cb880b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:14:01 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 04:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a229db433d9600f62d1e04fd517749652a5a0fad9b51bc8cf426c5c12d5862`  
		Last Modified: Wed, 05 Oct 2022 04:16:58 GMT  
		Size: 122.6 MB (122639897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:dc9cd6d5a597a14a193d495d02bbe2ca60dab2a5fb01563ee27a1c1f6c1ab698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142495823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c69cb56c8673f04379daacda1ad823d719da1eff37bd01ee0f8876d5082e3b4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:57:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:57:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:57:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 05:04:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 05:04:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad2fd8944c2866a23946bb173e0e383044efc6cc17556c88712007d29fbb742`  
		Last Modified: Wed, 05 Oct 2022 05:05:36 GMT  
		Size: 2.2 MB (2228860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38a8a3a11ec4c902839113094aeae003ce8902db81798d38d1b6c5db8f8622`  
		Last Modified: Wed, 05 Oct 2022 05:06:02 GMT  
		Size: 113.7 MB (113687764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4b3d928fb5fc3a6090c038c8ec0400bba3f654ebe99fd184ca1dada4fb302f5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148487307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d18bd6333c8505e700b3e5c9662dd874d29407bc51a3928b4dc300c0e52c096`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:57 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 03:02:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:02:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa0ca1db3a8b43b540209193186012fdcec24454da49b7db9e32304fd1050e2`  
		Last Modified: Wed, 05 Oct 2022 03:04:58 GMT  
		Size: 116.2 MB (116213264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-bullseye` - linux; 386

```console
$ docker pull julia@sha256:eed1e43b274fbd25a321d54d93d1ea23add302e972578319e113c349aa7020fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154813677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790d2c8a134679f481fdf4a79866bd51d0384c7790c84bb5e94ee3137378527f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:45 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 02:11:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:11:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecaaeb59bbf6af29174938b9dc562aafa64c6ea714d9a0bafec2e63468275be`  
		Last Modified: Wed, 05 Oct 2022 02:13:39 GMT  
		Size: 120.1 MB (120090666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-buster`

```console
$ docker pull julia@sha256:bb43e032042cf982789be0ae817abffd13232e9e1b4ee0edff86d6e6e5b7b65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6-buster` - linux; amd64

```console
$ docker pull julia@sha256:8c172c357cab39d3986bc31c459062632d4fb40302fc7e7d948ed2dab6aec2fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154256168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0d597469d82b861fd7c7a6dc077831e7d2a3b62b6174fc94119d7ea00efe88`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:14:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 04:14:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:14:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c2c91b60a243ec7a657c586ba51a4c16b8d24a1d693ebb322bcc1bdfcf1b`  
		Last Modified: Wed, 05 Oct 2022 04:15:58 GMT  
		Size: 4.5 MB (4468448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02d04b1fded9c4e8a5ff4bfcfb755bab6b5c7e4e412c8df08673f85c5281f51`  
		Last Modified: Wed, 05 Oct 2022 04:17:27 GMT  
		Size: 122.6 MB (122649677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:3240456114bca2eadd2f66e4a401b9bc920dfeb4e7aa086511d274566c2c9987
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140254034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a6215ac16f77b7648b212b55b6321f1b52458c1c319b0c20fdf4b358f37214`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:59:18 GMT
ADD file:3cde948f83f960927e2aa8be792b46726d7c3cb7a5250167816f138165e1ed3f in / 
# Tue, 04 Oct 2022 23:59:18 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 05:04:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 05:04:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 05:04:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 05:04:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 05:04:41 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 05:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 05:05:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4d0206a59e12f0afd97e080863f8788c54ecd251e26b9e6dd5d6db4d56cef8cd`  
		Last Modified: Wed, 05 Oct 2022 00:06:03 GMT  
		Size: 22.7 MB (22746557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cc1e4e7d8c0d012bf05d9f394246ec6d261c36f3818911ab757cf595a1d532`  
		Last Modified: Wed, 05 Oct 2022 05:06:15 GMT  
		Size: 3.8 MB (3811719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bcc60b9762e3688558a156f62aefa39dae719d11df59441c6df25026398a9d`  
		Last Modified: Wed, 05 Oct 2022 05:06:39 GMT  
		Size: 113.7 MB (113695758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:75b2fad80d1bfb263a4dc0f323098e103e7643a88753cbb3428d69815212fa12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146481091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d8c24c961e60edc2d09e503d73d780b4dca20c772f494db40c642aea1bb871`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:02:24 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 03:02:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:02:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d6e174971e58cca6ef91341e0bab0511c3017f7a3a1d3c3dcb897c9d14cb`  
		Last Modified: Wed, 05 Oct 2022 03:05:27 GMT  
		Size: 116.2 MB (116222248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-buster` - linux; 386

```console
$ docker pull julia@sha256:574d6f13c08f65dffa75b173e6d1ce3657a739a1f35a1f5d63b71d241aef6f3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152517536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8abee8420da39b9ad3beaa455b403cb1a845b38d5af926d71f5a730a639f42`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:11:11 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 02:11:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:11:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade3a40e842da49cc8b9b9ca7522251c6d8c76892f7b39998aa81d57043645af`  
		Last Modified: Wed, 05 Oct 2022 02:14:06 GMT  
		Size: 120.1 MB (120103158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore`

```console
$ docker pull julia@sha256:a5e0303651b5eb216171932608ca68c51c03ec4d220582f1f7180adb8ae996cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.6-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:34f0ef538a98f4fceb49284f465d6a02973f403df639dd0f59b16e4835b1b4d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550890943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad32493df8519291d48f606f52bfa0bf7427fc178e352f096ff27ae2d6532b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:06:42 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:06:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:06:44 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:07:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4e0cf35d121019206cf2b70cbd13b415069e0526d66b8139de599cd62583d`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fe6483e5d57d263acfaabb07480e724baa8eb33dff561897286ccc91a8af9`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2565c05345376ffdfa512de2c9201d03ae98a827b49dccb5f3d74b060e2e`  
		Last Modified: Wed, 12 Oct 2022 15:12:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6030bfa6a596b3bd6e1dd58900e61d21995691eff90baf3f170f21261cc27c`  
		Last Modified: Wed, 12 Oct 2022 15:12:58 GMT  
		Size: 134.7 MB (134660486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfc11771396e7dab867c32ba66aa2e14c1fc5ab6c66509cc9e7f074ff249e5`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:6d50044816a3d6c929350dffa15a8bf5ca108f16288ace088a43f68cff1c9941
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2845581797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8c3f74e0120f6ea3b2bd61d80a7e65d88746a9cdbdcfe3b11dd1f9718d9bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:08:14 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:08:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:08:16 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:10:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5521024befbc8e402dfb54dba5a88b96791543090d98bf68992b52259541b`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed136e7af2fef739ea1164a8f3535d71d81d70b2f355f6e2464958fdf1936053`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dd422d2bef6b74e6bfc13cdfb305f46baf9e23c61b413dea44b2dff639d1e`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985cc5fc071101024b8c101fcea4398edc11c3aff42cbec8f1a6d10f7ddc916`  
		Last Modified: Wed, 12 Oct 2022 15:13:38 GMT  
		Size: 134.4 MB (134410742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d6c7151cb560c7cb9bdc9e428c5195f18ed002469b66cf823d09ca174c1f4`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-1809`

```console
$ docker pull julia@sha256:daf9a85f64e64678b48069731840d91af63fb9159567c7d6a3418d419834da03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `julia:1.6-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:6d50044816a3d6c929350dffa15a8bf5ca108f16288ace088a43f68cff1c9941
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2845581797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8c3f74e0120f6ea3b2bd61d80a7e65d88746a9cdbdcfe3b11dd1f9718d9bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:08:14 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:08:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:08:16 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:10:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5521024befbc8e402dfb54dba5a88b96791543090d98bf68992b52259541b`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed136e7af2fef739ea1164a8f3535d71d81d70b2f355f6e2464958fdf1936053`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dd422d2bef6b74e6bfc13cdfb305f46baf9e23c61b413dea44b2dff639d1e`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985cc5fc071101024b8c101fcea4398edc11c3aff42cbec8f1a6d10f7ddc916`  
		Last Modified: Wed, 12 Oct 2022 15:13:38 GMT  
		Size: 134.4 MB (134410742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d6c7151cb560c7cb9bdc9e428c5195f18ed002469b66cf823d09ca174c1f4`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0d398838d950ef83d4894ac45ccc72fc3fb21c9102230a5227370e005593bbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `julia:1.6-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:34f0ef538a98f4fceb49284f465d6a02973f403df639dd0f59b16e4835b1b4d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550890943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad32493df8519291d48f606f52bfa0bf7427fc178e352f096ff27ae2d6532b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:06:42 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:06:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:06:44 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:07:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4e0cf35d121019206cf2b70cbd13b415069e0526d66b8139de599cd62583d`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fe6483e5d57d263acfaabb07480e724baa8eb33dff561897286ccc91a8af9`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2565c05345376ffdfa512de2c9201d03ae98a827b49dccb5f3d74b060e2e`  
		Last Modified: Wed, 12 Oct 2022 15:12:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6030bfa6a596b3bd6e1dd58900e61d21995691eff90baf3f170f21261cc27c`  
		Last Modified: Wed, 12 Oct 2022 15:12:58 GMT  
		Size: 134.7 MB (134660486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfc11771396e7dab867c32ba66aa2e14c1fc5ab6c66509cc9e7f074ff249e5`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7`

```console
$ docker pull julia@sha256:6be6530120577d69e76c19d7765e8a2a0b92935150423abfada066f676c95958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.6.7` - linux; amd64

```console
$ docker pull julia@sha256:69fc7255c083cfaea291719eadc3f24d8cc395bb75893638d243605ac1424937
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156486591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634db3704dfd188d5aa7a0f5bfde32f598c561e5394fdfb880f2611d53cb880b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:14:01 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 04:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a229db433d9600f62d1e04fd517749652a5a0fad9b51bc8cf426c5c12d5862`  
		Last Modified: Wed, 05 Oct 2022 04:16:58 GMT  
		Size: 122.6 MB (122639897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - linux; arm variant v7

```console
$ docker pull julia@sha256:dc9cd6d5a597a14a193d495d02bbe2ca60dab2a5fb01563ee27a1c1f6c1ab698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142495823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c69cb56c8673f04379daacda1ad823d719da1eff37bd01ee0f8876d5082e3b4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:57:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:57:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:57:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 05:04:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 05:04:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad2fd8944c2866a23946bb173e0e383044efc6cc17556c88712007d29fbb742`  
		Last Modified: Wed, 05 Oct 2022 05:05:36 GMT  
		Size: 2.2 MB (2228860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38a8a3a11ec4c902839113094aeae003ce8902db81798d38d1b6c5db8f8622`  
		Last Modified: Wed, 05 Oct 2022 05:06:02 GMT  
		Size: 113.7 MB (113687764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4b3d928fb5fc3a6090c038c8ec0400bba3f654ebe99fd184ca1dada4fb302f5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148487307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d18bd6333c8505e700b3e5c9662dd874d29407bc51a3928b4dc300c0e52c096`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:57 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 03:02:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:02:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa0ca1db3a8b43b540209193186012fdcec24454da49b7db9e32304fd1050e2`  
		Last Modified: Wed, 05 Oct 2022 03:04:58 GMT  
		Size: 116.2 MB (116213264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - linux; 386

```console
$ docker pull julia@sha256:eed1e43b274fbd25a321d54d93d1ea23add302e972578319e113c349aa7020fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154813677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790d2c8a134679f481fdf4a79866bd51d0384c7790c84bb5e94ee3137378527f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:45 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 02:11:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:11:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecaaeb59bbf6af29174938b9dc562aafa64c6ea714d9a0bafec2e63468275be`  
		Last Modified: Wed, 05 Oct 2022 02:13:39 GMT  
		Size: 120.1 MB (120090666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:34f0ef538a98f4fceb49284f465d6a02973f403df639dd0f59b16e4835b1b4d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550890943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad32493df8519291d48f606f52bfa0bf7427fc178e352f096ff27ae2d6532b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:06:42 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:06:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:06:44 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:07:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4e0cf35d121019206cf2b70cbd13b415069e0526d66b8139de599cd62583d`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fe6483e5d57d263acfaabb07480e724baa8eb33dff561897286ccc91a8af9`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2565c05345376ffdfa512de2c9201d03ae98a827b49dccb5f3d74b060e2e`  
		Last Modified: Wed, 12 Oct 2022 15:12:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6030bfa6a596b3bd6e1dd58900e61d21995691eff90baf3f170f21261cc27c`  
		Last Modified: Wed, 12 Oct 2022 15:12:58 GMT  
		Size: 134.7 MB (134660486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfc11771396e7dab867c32ba66aa2e14c1fc5ab6c66509cc9e7f074ff249e5`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:6d50044816a3d6c929350dffa15a8bf5ca108f16288ace088a43f68cff1c9941
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2845581797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8c3f74e0120f6ea3b2bd61d80a7e65d88746a9cdbdcfe3b11dd1f9718d9bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:08:14 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:08:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:08:16 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:10:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5521024befbc8e402dfb54dba5a88b96791543090d98bf68992b52259541b`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed136e7af2fef739ea1164a8f3535d71d81d70b2f355f6e2464958fdf1936053`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dd422d2bef6b74e6bfc13cdfb305f46baf9e23c61b413dea44b2dff639d1e`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985cc5fc071101024b8c101fcea4398edc11c3aff42cbec8f1a6d10f7ddc916`  
		Last Modified: Wed, 12 Oct 2022 15:13:38 GMT  
		Size: 134.4 MB (134410742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d6c7151cb560c7cb9bdc9e428c5195f18ed002469b66cf823d09ca174c1f4`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine`

```console
$ docker pull julia@sha256:2589757b00b345796a9d19ae2d006b721016da0eb56891e922eeb0f7067dbbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.7-alpine` - linux; amd64

```console
$ docker pull julia@sha256:5698ae540981aea211af20caf022be767a8aaf2ab21ca02ba71c6155b0be6247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca6d1c792a16baf4c80e75d5521042da08c49a9d4f16977cd682a8b2ec7014b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:48:18 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 06 Oct 2022 22:55:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:55:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2155182571b34a72eb201caaf6b72c0c4865409b4d31c1adf7bb7a9ad64c3ea0`  
		Last Modified: Thu, 06 Oct 2022 22:58:30 GMT  
		Size: 121.8 MB (121828697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine3.15`

```console
$ docker pull julia@sha256:dabdc633888297b0fff4b09b1e16f0020a89e7a35d123f0e07f76dd22c50c94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.7-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:e94cc93368b7ebde8e1ebf8b06ec2da396592b46d9aead799b9ce8b9155c1b09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124652062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc78044f85060bcff7a6c4d9e9d40545c87106711bbe9ddbfebed0c9cd32917`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:55:56 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 06 Oct 2022 22:56:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:56:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b56890552fa59b38e90510ee05c9235377bca048c4b6acdf5b6bbf015c17263`  
		Last Modified: Thu, 06 Oct 2022 22:59:05 GMT  
		Size: 121.8 MB (121828550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-alpine3.16`

```console
$ docker pull julia@sha256:2589757b00b345796a9d19ae2d006b721016da0eb56891e922eeb0f7067dbbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.6.7-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:5698ae540981aea211af20caf022be767a8aaf2ab21ca02ba71c6155b0be6247
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124634751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca6d1c792a16baf4c80e75d5521042da08c49a9d4f16977cd682a8b2ec7014b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:48:18 GMT
ENV JULIA_VERSION=1.6.7
# Thu, 06 Oct 2022 22:55:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.6/julia-1.6.7-musl-x86_64.tar.gz'; 			sha256='d71ccc5aa36cf691616a40bf6fb960fac5620ce53d2f90a95947b90dec509433'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:55:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2155182571b34a72eb201caaf6b72c0c4865409b4d31c1adf7bb7a9ad64c3ea0`  
		Last Modified: Thu, 06 Oct 2022 22:58:30 GMT  
		Size: 121.8 MB (121828697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-bullseye`

```console
$ docker pull julia@sha256:2657d5360026d785085a0bd46387540d91281e0f00144b6cc097f290b5c31c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6.7-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:69fc7255c083cfaea291719eadc3f24d8cc395bb75893638d243605ac1424937
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156486591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634db3704dfd188d5aa7a0f5bfde32f598c561e5394fdfb880f2611d53cb880b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:14:01 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 04:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a229db433d9600f62d1e04fd517749652a5a0fad9b51bc8cf426c5c12d5862`  
		Last Modified: Wed, 05 Oct 2022 04:16:58 GMT  
		Size: 122.6 MB (122639897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-bullseye` - linux; arm variant v7

```console
$ docker pull julia@sha256:dc9cd6d5a597a14a193d495d02bbe2ca60dab2a5fb01563ee27a1c1f6c1ab698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142495823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c69cb56c8673f04379daacda1ad823d719da1eff37bd01ee0f8876d5082e3b4`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:58:46 GMT
ADD file:ca1bf27f17594a91224a252bd446f97c3b898210c571f2f26fa2e723d2bf521e in / 
# Tue, 04 Oct 2022 23:58:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:57:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:57:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:57:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:57:59 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 05:04:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 05:04:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2bc64aeac2e429577e497affc8a416d2fc59158aa967f07aced793368e19455f`  
		Last Modified: Wed, 05 Oct 2022 00:05:09 GMT  
		Size: 26.6 MB (26579199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad2fd8944c2866a23946bb173e0e383044efc6cc17556c88712007d29fbb742`  
		Last Modified: Wed, 05 Oct 2022 05:05:36 GMT  
		Size: 2.2 MB (2228860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b38a8a3a11ec4c902839113094aeae003ce8902db81798d38d1b6c5db8f8622`  
		Last Modified: Wed, 05 Oct 2022 05:06:02 GMT  
		Size: 113.7 MB (113687764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4b3d928fb5fc3a6090c038c8ec0400bba3f654ebe99fd184ca1dada4fb302f5e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148487307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d18bd6333c8505e700b3e5c9662dd874d29407bc51a3928b4dc300c0e52c096`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:57 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 03:02:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:02:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa0ca1db3a8b43b540209193186012fdcec24454da49b7db9e32304fd1050e2`  
		Last Modified: Wed, 05 Oct 2022 03:04:58 GMT  
		Size: 116.2 MB (116213264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-bullseye` - linux; 386

```console
$ docker pull julia@sha256:eed1e43b274fbd25a321d54d93d1ea23add302e972578319e113c349aa7020fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154813677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790d2c8a134679f481fdf4a79866bd51d0384c7790c84bb5e94ee3137378527f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:45 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 02:11:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:11:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecaaeb59bbf6af29174938b9dc562aafa64c6ea714d9a0bafec2e63468275be`  
		Last Modified: Wed, 05 Oct 2022 02:13:39 GMT  
		Size: 120.1 MB (120090666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-buster`

```console
$ docker pull julia@sha256:bb43e032042cf982789be0ae817abffd13232e9e1b4ee0edff86d6e6e5b7b65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.6.7-buster` - linux; amd64

```console
$ docker pull julia@sha256:8c172c357cab39d3986bc31c459062632d4fb40302fc7e7d948ed2dab6aec2fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154256168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0d597469d82b861fd7c7a6dc077831e7d2a3b62b6174fc94119d7ea00efe88`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:14:21 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 04:14:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:14:37 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c2c91b60a243ec7a657c586ba51a4c16b8d24a1d693ebb322bcc1bdfcf1b`  
		Last Modified: Wed, 05 Oct 2022 04:15:58 GMT  
		Size: 4.5 MB (4468448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02d04b1fded9c4e8a5ff4bfcfb755bab6b5c7e4e412c8df08673f85c5281f51`  
		Last Modified: Wed, 05 Oct 2022 04:17:27 GMT  
		Size: 122.6 MB (122649677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:3240456114bca2eadd2f66e4a401b9bc920dfeb4e7aa086511d274566c2c9987
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140254034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a6215ac16f77b7648b212b55b6321f1b52458c1c319b0c20fdf4b358f37214`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:59:18 GMT
ADD file:3cde948f83f960927e2aa8be792b46726d7c3cb7a5250167816f138165e1ed3f in / 
# Tue, 04 Oct 2022 23:59:18 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 05:04:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 05:04:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 05:04:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 05:04:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 05:04:41 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 05:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 05:05:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4d0206a59e12f0afd97e080863f8788c54ecd251e26b9e6dd5d6db4d56cef8cd`  
		Last Modified: Wed, 05 Oct 2022 00:06:03 GMT  
		Size: 22.7 MB (22746557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cc1e4e7d8c0d012bf05d9f394246ec6d261c36f3818911ab757cf595a1d532`  
		Last Modified: Wed, 05 Oct 2022 05:06:15 GMT  
		Size: 3.8 MB (3811719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bcc60b9762e3688558a156f62aefa39dae719d11df59441c6df25026398a9d`  
		Last Modified: Wed, 05 Oct 2022 05:06:39 GMT  
		Size: 113.7 MB (113695758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:75b2fad80d1bfb263a4dc0f323098e103e7643a88753cbb3428d69815212fa12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146481091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06d8c24c961e60edc2d09e503d73d780b4dca20c772f494db40c642aea1bb871`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:02:24 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 03:02:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:02:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1d6e174971e58cca6ef91341e0bab0511c3017f7a3a1d3c3dcb897c9d14cb`  
		Last Modified: Wed, 05 Oct 2022 03:05:27 GMT  
		Size: 116.2 MB (116222248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-buster` - linux; 386

```console
$ docker pull julia@sha256:574d6f13c08f65dffa75b173e6d1ce3657a739a1f35a1f5d63b71d241aef6f3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152517536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8abee8420da39b9ad3beaa455b403cb1a845b38d5af926d71f5a730a639f42`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:11:11 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 05 Oct 2022 02:11:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.7-linux-x86_64.tar.gz'; 			sha256='6c4522d595e4cbcd00157ac458a72f8aec01757053d2073f99daa39e442b2a36'; 			;; 		'armhf') 			url='https://julialang-s3.julialang.org/bin/linux/armv7l/1.6/julia-1.6.7-linux-armv7l.tar.gz'; 			sha256='67db7e1f4ad4b9676c26a4659ede8bb9a174346fe22b236f568028c63f02ed2a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.6/julia-1.6.7-linux-aarch64.tar.gz'; 			sha256='8746d561cbe35e1b83739a84b2637a1d2348728b1d94d76629ad98ff76da6cea'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.6/julia-1.6.7-linux-i686.tar.gz'; 			sha256='d11edad41d2cf4784647e2ac9e304c189bed914cbf38ce4008c668ba789e6df9'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:11:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade3a40e842da49cc8b9b9ca7522251c6d8c76892f7b39998aa81d57043645af`  
		Last Modified: Wed, 05 Oct 2022 02:14:06 GMT  
		Size: 120.1 MB (120103158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore`

```console
$ docker pull julia@sha256:a5e0303651b5eb216171932608ca68c51c03ec4d220582f1f7180adb8ae996cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.6.7-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:34f0ef538a98f4fceb49284f465d6a02973f403df639dd0f59b16e4835b1b4d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550890943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad32493df8519291d48f606f52bfa0bf7427fc178e352f096ff27ae2d6532b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:06:42 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:06:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:06:44 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:07:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4e0cf35d121019206cf2b70cbd13b415069e0526d66b8139de599cd62583d`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fe6483e5d57d263acfaabb07480e724baa8eb33dff561897286ccc91a8af9`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2565c05345376ffdfa512de2c9201d03ae98a827b49dccb5f3d74b060e2e`  
		Last Modified: Wed, 12 Oct 2022 15:12:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6030bfa6a596b3bd6e1dd58900e61d21995691eff90baf3f170f21261cc27c`  
		Last Modified: Wed, 12 Oct 2022 15:12:58 GMT  
		Size: 134.7 MB (134660486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfc11771396e7dab867c32ba66aa2e14c1fc5ab6c66509cc9e7f074ff249e5`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.6.7-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:6d50044816a3d6c929350dffa15a8bf5ca108f16288ace088a43f68cff1c9941
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2845581797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8c3f74e0120f6ea3b2bd61d80a7e65d88746a9cdbdcfe3b11dd1f9718d9bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:08:14 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:08:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:08:16 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:10:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5521024befbc8e402dfb54dba5a88b96791543090d98bf68992b52259541b`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed136e7af2fef739ea1164a8f3535d71d81d70b2f355f6e2464958fdf1936053`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dd422d2bef6b74e6bfc13cdfb305f46baf9e23c61b413dea44b2dff639d1e`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985cc5fc071101024b8c101fcea4398edc11c3aff42cbec8f1a6d10f7ddc916`  
		Last Modified: Wed, 12 Oct 2022 15:13:38 GMT  
		Size: 134.4 MB (134410742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d6c7151cb560c7cb9bdc9e428c5195f18ed002469b66cf823d09ca174c1f4`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-1809`

```console
$ docker pull julia@sha256:daf9a85f64e64678b48069731840d91af63fb9159567c7d6a3418d419834da03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `julia:1.6.7-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:6d50044816a3d6c929350dffa15a8bf5ca108f16288ace088a43f68cff1c9941
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2845581797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a8c3f74e0120f6ea3b2bd61d80a7e65d88746a9cdbdcfe3b11dd1f9718d9bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:08:14 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:08:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:08:16 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:10:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:10:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f5521024befbc8e402dfb54dba5a88b96791543090d98bf68992b52259541b`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed136e7af2fef739ea1164a8f3535d71d81d70b2f355f6e2464958fdf1936053`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505dd422d2bef6b74e6bfc13cdfb305f46baf9e23c61b413dea44b2dff639d1e`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c985cc5fc071101024b8c101fcea4398edc11c3aff42cbec8f1a6d10f7ddc916`  
		Last Modified: Wed, 12 Oct 2022 15:13:38 GMT  
		Size: 134.4 MB (134410742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44d6c7151cb560c7cb9bdc9e428c5195f18ed002469b66cf823d09ca174c1f4`  
		Last Modified: Wed, 12 Oct 2022 15:13:08 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.6.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:0d398838d950ef83d4894ac45ccc72fc3fb21c9102230a5227370e005593bbc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `julia:1.6.7-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:34f0ef538a98f4fceb49284f465d6a02973f403df639dd0f59b16e4835b1b4d7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2550890943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad32493df8519291d48f606f52bfa0bf7427fc178e352f096ff27ae2d6532b0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:06:42 GMT
ENV JULIA_VERSION=1.6.7
# Wed, 12 Oct 2022 15:06:43 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.6/julia-1.6.7-win64.exe
# Wed, 12 Oct 2022 15:06:44 GMT
ENV JULIA_SHA256=20a4bdca8314a6193472ee29f470ba02a1f8ffd7a803342896fcbbf61bf3d4c8
# Wed, 12 Oct 2022 15:07:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:07:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4e0cf35d121019206cf2b70cbd13b415069e0526d66b8139de599cd62583d`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:359fe6483e5d57d263acfaabb07480e724baa8eb33dff561897286ccc91a8af9`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942c2565c05345376ffdfa512de2c9201d03ae98a827b49dccb5f3d74b060e2e`  
		Last Modified: Wed, 12 Oct 2022 15:12:28 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6030bfa6a596b3bd6e1dd58900e61d21995691eff90baf3f170f21261cc27c`  
		Last Modified: Wed, 12 Oct 2022 15:12:58 GMT  
		Size: 134.7 MB (134660486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adfc11771396e7dab867c32ba66aa2e14c1fc5ab6c66509cc9e7f074ff249e5`  
		Last Modified: Wed, 12 Oct 2022 15:12:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8`

```console
$ docker pull julia@sha256:31b661ff9b0bacc635afebf74a41061e761091dfa4e0f60e3f5db62b0e748862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.8` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-alpine`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8-alpine` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-alpine3.15`

```console
$ docker pull julia@sha256:38914c91fdc9be54e8fee495b02ec2c618b398a7715a5019b076237ce7ccc565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:be7a89dfc616b44b83cb9e2e7413ef0296974f541602183a9504eb98c0dfd67f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149958895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c947abb57660db81dd3e216198ef24473b06894a4307c969bbf52619c56afa`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:48:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:48:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7952d73a20c790439007f53998172937cbf1b838ab52ce6411d56fa0cd4d68a`  
		Last Modified: Thu, 06 Oct 2022 22:57:55 GMT  
		Size: 147.1 MB (147135383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-alpine3.16`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-bullseye`

```console
$ docker pull julia@sha256:183b4b5727f6996d59374eb4dd8742d12be71b32641bb32c2ef9e3371817731a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-buster`

```console
$ docker pull julia@sha256:449fb68a71c39009c7a157e8c3e112bbf5f18a9c41c39d4ac290fd8cd3f53187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8-buster` - linux; amd64

```console
$ docker pull julia@sha256:4fae4331e7e21afda51912a3eaee115723f85a5513fa23aef1ed8b75c53d0062
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177432150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abf5b0b7bbc388655b6555168e61f5c1a7de354aeb23740b8dfb0496c80e8b6`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c2c91b60a243ec7a657c586ba51a4c16b8d24a1d693ebb322bcc1bdfcf1b`  
		Last Modified: Wed, 05 Oct 2022 04:15:58 GMT  
		Size: 4.5 MB (4468448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7762e9536e599b6aafe5001040d2ee204076444131dbc5b69ed1910652e7220`  
		Last Modified: Wed, 05 Oct 2022 04:16:20 GMT  
		Size: 145.8 MB (145825659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1e5f54d0ad4fd36bd1d679e074391447933dc8a127970197083d71c16a8a568a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169894074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f5f6260ec64d1f7c8dcf2342aab66630ea433847a0e919f53868e8c53871e7`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8297636379925d4f7ea1fdac2965d49b5cac0c8b948da968e5bea62d5b0757`  
		Last Modified: Wed, 05 Oct 2022 03:04:23 GMT  
		Size: 139.6 MB (139635231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-buster` - linux; 386

```console
$ docker pull julia@sha256:37a1da12330b7d038acddfc55e8980f999a87cbada9b43ace6cfb4e28ea2f350
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175134939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dabb27a643c5ceb1f4eedc67f354efa8ba52d127c5450ddcf4931bc1a32518`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:18 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb28420c7c0fd820677e95822c0e1e9da492a9d8a6950338327051151adb5d`  
		Last Modified: Wed, 05 Oct 2022 02:13:06 GMT  
		Size: 142.7 MB (142720561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-windowsservercore`

```console
$ docker pull julia@sha256:5ba56e049b8e09c7a05d0620b12a3121e98ce39ac100b6df6b14e151dde32fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.8-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-windowsservercore-1809`

```console
$ docker pull julia@sha256:0891bbcecea522e4e7cb5b7a367b6e00e3a2323d37bd6a48b704d415ae3aea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `julia:1.8-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1d40145cf504997e2e7526e95bd865147d1c11e0ea1e2d3a098aafeaade3fe11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `julia:1.8-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2`

```console
$ docker pull julia@sha256:31b661ff9b0bacc635afebf74a41061e761091dfa4e0f60e3f5db62b0e748862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.8.2` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-alpine`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8.2-alpine` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-alpine3.15`

```console
$ docker pull julia@sha256:38914c91fdc9be54e8fee495b02ec2c618b398a7715a5019b076237ce7ccc565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8.2-alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:be7a89dfc616b44b83cb9e2e7413ef0296974f541602183a9504eb98c0dfd67f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149958895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c947abb57660db81dd3e216198ef24473b06894a4307c969bbf52619c56afa`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:48:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:48:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7952d73a20c790439007f53998172937cbf1b838ab52ce6411d56fa0cd4d68a`  
		Last Modified: Thu, 06 Oct 2022 22:57:55 GMT  
		Size: 147.1 MB (147135383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-alpine3.16`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:1.8.2-alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-bullseye`

```console
$ docker pull julia@sha256:183b4b5727f6996d59374eb4dd8742d12be71b32641bb32c2ef9e3371817731a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8.2-bullseye` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2-bullseye` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-buster`

```console
$ docker pull julia@sha256:449fb68a71c39009c7a157e8c3e112bbf5f18a9c41c39d4ac290fd8cd3f53187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.8.2-buster` - linux; amd64

```console
$ docker pull julia@sha256:4fae4331e7e21afda51912a3eaee115723f85a5513fa23aef1ed8b75c53d0062
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177432150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abf5b0b7bbc388655b6555168e61f5c1a7de354aeb23740b8dfb0496c80e8b6`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c2c91b60a243ec7a657c586ba51a4c16b8d24a1d693ebb322bcc1bdfcf1b`  
		Last Modified: Wed, 05 Oct 2022 04:15:58 GMT  
		Size: 4.5 MB (4468448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7762e9536e599b6aafe5001040d2ee204076444131dbc5b69ed1910652e7220`  
		Last Modified: Wed, 05 Oct 2022 04:16:20 GMT  
		Size: 145.8 MB (145825659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1e5f54d0ad4fd36bd1d679e074391447933dc8a127970197083d71c16a8a568a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169894074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f5f6260ec64d1f7c8dcf2342aab66630ea433847a0e919f53868e8c53871e7`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8297636379925d4f7ea1fdac2965d49b5cac0c8b948da968e5bea62d5b0757`  
		Last Modified: Wed, 05 Oct 2022 03:04:23 GMT  
		Size: 139.6 MB (139635231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2-buster` - linux; 386

```console
$ docker pull julia@sha256:37a1da12330b7d038acddfc55e8980f999a87cbada9b43ace6cfb4e28ea2f350
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175134939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dabb27a643c5ceb1f4eedc67f354efa8ba52d127c5450ddcf4931bc1a32518`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:18 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb28420c7c0fd820677e95822c0e1e9da492a9d8a6950338327051151adb5d`  
		Last Modified: Wed, 05 Oct 2022 02:13:06 GMT  
		Size: 142.7 MB (142720561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-windowsservercore`

```console
$ docker pull julia@sha256:5ba56e049b8e09c7a05d0620b12a3121e98ce39ac100b6df6b14e151dde32fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1.8.2-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.8.2-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-windowsservercore-1809`

```console
$ docker pull julia@sha256:0891bbcecea522e4e7cb5b7a367b6e00e3a2323d37bd6a48b704d415ae3aea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `julia:1.8.2-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.8.2-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1d40145cf504997e2e7526e95bd865147d1c11e0ea1e2d3a098aafeaade3fe11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `julia:1.8.2-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine3.15`

```console
$ docker pull julia@sha256:38914c91fdc9be54e8fee495b02ec2c618b398a7715a5019b076237ce7ccc565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.15` - linux; amd64

```console
$ docker pull julia@sha256:be7a89dfc616b44b83cb9e2e7413ef0296974f541602183a9504eb98c0dfd67f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149958895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c947abb57660db81dd3e216198ef24473b06894a4307c969bbf52619c56afa`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:54 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:48:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:48:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7952d73a20c790439007f53998172937cbf1b838ab52ce6411d56fa0cd4d68a`  
		Last Modified: Thu, 06 Oct 2022 22:57:55 GMT  
		Size: 147.1 MB (147135383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:alpine3.16`

```console
$ docker pull julia@sha256:0f20015a8db8fecc41942a842f1a2786238a2eb12451d850cfacd09d045fcf31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `julia:alpine3.16` - linux; amd64

```console
$ docker pull julia@sha256:13218a325a9c887ecef20ddb6c466771e848aeb988d1f643686c73eedd106afb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149941305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8f43b13a61779c303d00270995686a8379abbcf51516066c0600997427592f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 06 Oct 2022 22:47:30 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 06 Oct 2022 22:47:30 GMT
ENV JULIA_VERSION=1.8.2
# Thu, 06 Oct 2022 22:47:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.8/julia-1.8.2-musl-x86_64.tar.gz'; 			sha256='9a50f90f30254b588be74e1cb983f6408b0ed81f28f7cd7077a0eefc7f33e04a'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version
# Thu, 06 Oct 2022 22:47:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2882d2a8dfa789bca23e47bfb1771aeecb1a9a98fd41926bdfc49aa1771f659`  
		Last Modified: Thu, 06 Oct 2022 22:57:10 GMT  
		Size: 147.1 MB (147135251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bullseye`

```console
$ docker pull julia@sha256:183b4b5727f6996d59374eb4dd8742d12be71b32641bb32c2ef9e3371817731a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:bullseye` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:bullseye` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:buster`

```console
$ docker pull julia@sha256:449fb68a71c39009c7a157e8c3e112bbf5f18a9c41c39d4ac290fd8cd3f53187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:4fae4331e7e21afda51912a3eaee115723f85a5513fa23aef1ed8b75c53d0062
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177432150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abf5b0b7bbc388655b6555168e61f5c1a7de354aeb23740b8dfb0496c80e8b6`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:27:01 GMT
ADD file:706105a4a2ea63ba10911afb5998d321ff745f9bcedd2e2e8efcf33f5dad584b in / 
# Tue, 04 Oct 2022 23:27:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f6e04ba6531065d60cd73d6509ec153307f5cc6f95e72ca47745d37aef6380a7`  
		Last Modified: Tue, 04 Oct 2022 23:31:38 GMT  
		Size: 27.1 MB (27138043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf9c2c91b60a243ec7a657c586ba51a4c16b8d24a1d693ebb322bcc1bdfcf1b`  
		Last Modified: Wed, 05 Oct 2022 04:15:58 GMT  
		Size: 4.5 MB (4468448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7762e9536e599b6aafe5001040d2ee204076444131dbc5b69ed1910652e7220`  
		Last Modified: Wed, 05 Oct 2022 04:16:20 GMT  
		Size: 145.8 MB (145825659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1e5f54d0ad4fd36bd1d679e074391447933dc8a127970197083d71c16a8a568a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169894074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f5f6260ec64d1f7c8dcf2342aab66630ea433847a0e919f53868e8c53871e7`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:45:10 GMT
ADD file:5395cc8536f80a7cce6fbae552f35b892b152e1db2fce6274fc514d8fc77d7c9 in / 
# Tue, 04 Oct 2022 23:45:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:01:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:01:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:01:33 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:01:34 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:01:35 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c1ba50780a9bc2b2a8f3d639ceca4285c97f51fd1c51c783fe34e150ff35e60`  
		Last Modified: Tue, 04 Oct 2022 23:51:14 GMT  
		Size: 25.9 MB (25911903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e410967f644c335c9ba4865ddc128a10c8a2ddaa2f87531730e0dc3cfd45e10`  
		Last Modified: Wed, 05 Oct 2022 03:04:03 GMT  
		Size: 4.3 MB (4346940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8297636379925d4f7ea1fdac2965d49b5cac0c8b948da968e5bea62d5b0757`  
		Last Modified: Wed, 05 Oct 2022 03:04:23 GMT  
		Size: 139.6 MB (139635231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:37a1da12330b7d038acddfc55e8980f999a87cbada9b43ace6cfb4e28ea2f350
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175134939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dabb27a643c5ceb1f4eedc67f354efa8ba52d127c5450ddcf4931bc1a32518`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:40:08 GMT
ADD file:b1ef7e7f4c48770bde0d19751bb1624a887b657a5a5ab5d453fd5365b3448618 in / 
# Tue, 04 Oct 2022 23:40:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:10:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:10:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:10:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:10:17 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:10:18 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:38 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d1d1dd08a5009b10b72285f23ffd4c1978d3445cc3855d22f4112018b15a9420`  
		Last Modified: Tue, 04 Oct 2022 23:46:26 GMT  
		Size: 27.8 MB (27797501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:796da4c51cacb791da540589b88d5bf127f182fb0d4eb46530ca9ff61ea44fbc`  
		Last Modified: Wed, 05 Oct 2022 02:12:49 GMT  
		Size: 4.6 MB (4616877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fb28420c7c0fd820677e95822c0e1e9da492a9d8a6950338327051151adb5d`  
		Last Modified: Wed, 05 Oct 2022 02:13:06 GMT  
		Size: 142.7 MB (142720561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:latest`

```console
$ docker pull julia@sha256:31b661ff9b0bacc635afebf74a41061e761091dfa4e0f60e3f5db62b0e748862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:cdc9754be06bb12f9cebb0607d816301fe703bf4dd3733739be37187f71215f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179663313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5918cf923344b141197025617fe864b3d45bc4b5ec1352e0ef585cd758ea5`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 04:13:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 04:13:04 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 04:13:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 04:13:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8db5b67db5b783958c27725170387df2e17a26f5e5b84fe7021636aabb8f13`  
		Last Modified: Wed, 05 Oct 2022 04:15:21 GMT  
		Size: 2.4 MB (2426592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e24f4ec73c0cfaea322722d9d6b5e43e0ac35f4a17951e4138f0254224c9e3b`  
		Last Modified: Wed, 05 Oct 2022 04:15:43 GMT  
		Size: 145.8 MB (145816619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:33b4251a8bf7993015a405354f5332bb6cba73207b6aac76537b371e9403adde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171904321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f3fb8fb7952c37e99c19f40399cbbd45be5587a5052be79d6869733c2cbb3a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:00:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:00:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 03:00:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 03:00:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 03:00:57 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 03:01:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 03:01:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853a97676f7285584a0e561896a3873d942cfd731777779419c84fa1d8c86ea`  
		Last Modified: Wed, 05 Oct 2022 03:03:25 GMT  
		Size: 2.2 MB (2209648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7967c76989deab03d588e123221ba7846685870b5827aca9d26a0f9d0660f2`  
		Last Modified: Wed, 05 Oct 2022 03:03:45 GMT  
		Size: 139.6 MB (139630278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:4e9d1ab52fc070c135277e72358820b007387f2920c87e2fe0ec5ec19636727f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03341280ff73f8a9792a53c02def73b525a801ca5c1a22e01d31367974ff398a`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:40 GMT
ADD file:a66b7a182260a23fdb8b219600a8b48a5079997715006d9a5324dda11f9d0a7f in / 
# Tue, 04 Oct 2022 23:39:41 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:09:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:09:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 05 Oct 2022 02:09:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 02:09:38 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 05 Oct 2022 02:09:39 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 05 Oct 2022 02:10:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.2-linux-x86_64.tar.gz'; 			sha256='671cf3a450b63a717e1eedd7f69087e3856f015b2e146cb54928f19a3c05e796'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.2-linux-aarch64.tar.gz'; 			sha256='f91c276428ffb30acc209e0eb3e70b1c91260e887e11d4b66f5545084b530547'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.2-linux-i686.tar.gz'; 			sha256='3e407aef71bb075bbc7746a5d1f46116925490fb0cd992f453882e793fce6c29'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Wed, 05 Oct 2022 02:10:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:711839e532aa3f129f9cfaa5125d0e379ddefd47f3da44d0674372663dfc6a9b`  
		Last Modified: Tue, 04 Oct 2022 23:45:35 GMT  
		Size: 32.4 MB (32396290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3c219fc5cf0f7f315d7d4da59f0bcd3faf7f26e4fa4fe36fe6ac7906b61c12`  
		Last Modified: Wed, 05 Oct 2022 02:12:12 GMT  
		Size: 2.3 MB (2326721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b43bbfe1015f385874c054b3b87a961620ad44585f6c3d9c1e8399eac99c33`  
		Last Modified: Wed, 05 Oct 2022 02:12:30 GMT  
		Size: 142.7 MB (142715495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:5ba56e049b8e09c7a05d0620b12a3121e98ce39ac100b6df6b14e151dde32fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:0891bbcecea522e4e7cb5b7a367b6e00e3a2323d37bd6a48b704d415ae3aea6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1d40145cf504997e2e7526e95bd865147d1c11e0ea1e2d3a098aafeaade3fe11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
