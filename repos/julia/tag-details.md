<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1.0`](#julia10)
-	[`julia:1.0.5`](#julia105)
-	[`julia:1.0.5-buster`](#julia105-buster)
-	[`julia:1.0.5-stretch`](#julia105-stretch)
-	[`julia:1.0.5-windowsservercore-1809`](#julia105-windowsservercore-1809)
-	[`julia:1.0.5-windowsservercore-ltsc2016`](#julia105-windowsservercore-ltsc2016)
-	[`julia:1.0-buster`](#julia10-buster)
-	[`julia:1.0-stretch`](#julia10-stretch)
-	[`julia:1.0-windowsservercore-1809`](#julia10-windowsservercore-1809)
-	[`julia:1.0-windowsservercore-ltsc2016`](#julia10-windowsservercore-ltsc2016)
-	[`julia:1.4`](#julia14)
-	[`julia:1.4.2`](#julia142)
-	[`julia:1.4.2-buster`](#julia142-buster)
-	[`julia:1.4.2-windowsservercore-1809`](#julia142-windowsservercore-1809)
-	[`julia:1.4.2-windowsservercore-ltsc2016`](#julia142-windowsservercore-ltsc2016)
-	[`julia:1.4-buster`](#julia14-buster)
-	[`julia:1.4-windowsservercore-1809`](#julia14-windowsservercore-1809)
-	[`julia:1.4-windowsservercore-ltsc2016`](#julia14-windowsservercore-ltsc2016)
-	[`julia:1.5`](#julia15)
-	[`julia:1.5.0`](#julia150)
-	[`julia:1.5.0-beta1`](#julia150-beta1)
-	[`julia:1.5.0-beta1-buster`](#julia150-beta1-buster)
-	[`julia:1.5.0-beta1-windowsservercore-1809`](#julia150-beta1-windowsservercore-1809)
-	[`julia:1.5.0-beta1-windowsservercore-ltsc2016`](#julia150-beta1-windowsservercore-ltsc2016)
-	[`julia:1.5.0-buster`](#julia150-buster)
-	[`julia:1.5.0-windowsservercore-1809`](#julia150-windowsservercore-1809)
-	[`julia:1.5.0-windowsservercore-ltsc2016`](#julia150-windowsservercore-ltsc2016)
-	[`julia:1.5-buster`](#julia15-buster)
-	[`julia:1.5-rc`](#julia15-rc)
-	[`julia:1.5-rc-buster`](#julia15-rc-buster)
-	[`julia:1.5-rc-windowsservercore-1809`](#julia15-rc-windowsservercore-1809)
-	[`julia:1.5-rc-windowsservercore-ltsc2016`](#julia15-rc-windowsservercore-ltsc2016)
-	[`julia:1.5-windowsservercore-1809`](#julia15-windowsservercore-1809)
-	[`julia:1.5-windowsservercore-ltsc2016`](#julia15-windowsservercore-ltsc2016)
-	[`julia:1-buster`](#julia1-buster)
-	[`julia:1-windowsservercore-1809`](#julia1-windowsservercore-1809)
-	[`julia:1-windowsservercore-ltsc2016`](#julia1-windowsservercore-ltsc2016)
-	[`julia:buster`](#juliabuster)
-	[`julia:latest`](#julialatest)
-	[`julia:rc`](#juliarc)
-	[`julia:rc-buster`](#juliarc-buster)
-	[`julia:rc-windowsservercore-1809`](#juliarc-windowsservercore-1809)
-	[`julia:rc-windowsservercore-ltsc2016`](#juliarc-windowsservercore-ltsc2016)
-	[`julia:windowsservercore-1809`](#juliawindowsservercore-1809)
-	[`julia:windowsservercore-ltsc2016`](#juliawindowsservercore-ltsc2016)

## `julia:1`

```console
$ docker pull julia@sha256:6577631e3afb96c562b0649eb2a22ed6b8c2269e487fe6c50fd65938fcb1f9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0`

```console
$ docker pull julia@sha256:d0266b22a886d641e6a6f12859e9664e8563ee6e0374507ea9c4ce98a9a92e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.0` - linux; amd64

```console
$ docker pull julia@sha256:a7451826ead241068481f97261a1bf11aadbfb6d648ef3d676f72d21e642f7d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127097997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aca8f68b7e75d1021d3e3006be77e034615061fbd2ddabaed299b0de7b1522c`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:29 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1646a867aa17c939aeaef6e8bffc93361d9dcaac7d2f990068f03508cf29bdc`  
		Last Modified: Tue, 09 Jun 2020 07:09:01 GMT  
		Size: 95.6 MB (95563158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0` - linux; arm variant v7

```console
$ docker pull julia@sha256:bcf7766e456c8930ae20370c4d6d8a91dd26bc2ed3ba04e5b0c7e9204e2d924f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113617455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f1733b78167d6463e86c3778443e64c79c907e749e43d811fbd6dd8e4a5794`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:46:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:46:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 04:46:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:46:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 04:46:40 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 04:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 04:47:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a770ebabfd69d94d99a3dd0b3c4f87b64fca5e102575312774929eff99b51c0`  
		Last Modified: Tue, 09 Jun 2020 04:48:31 GMT  
		Size: 3.8 MB (3782747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53be19b37dff2a50445d792af5d381a870ab9d160b8976d298550b9ad8393d8a`  
		Last Modified: Tue, 09 Jun 2020 04:48:58 GMT  
		Size: 87.1 MB (87128795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7c3af80ff46b504788285e0e8ca36688e943ff524bff39802090c4843694c21d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110063821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360c01ef6037038896455058397e953d50fb518d8fec38d902ab7e6beff1f42`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:19:11 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 03:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d9c9f554133e1337121107c41f70af5bd91d9e152614e6fcb3d576e4a093a`  
		Last Modified: Tue, 09 Jun 2020 03:22:58 GMT  
		Size: 79.9 MB (79890958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0` - linux; 386

```console
$ docker pull julia@sha256:8150387e08dbb9fbb3b55792afa31de3d46c8791feb3aa773b9fcdcf4d17bc60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4e88755e4de826b4587b435b9c5bafcda02036cc90969547284ee93481c1c9`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 18:07:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 15 May 2020 18:07:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 18:07:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 15 May 2020 18:07:42 GMT
ENV JULIA_VERSION=1.0.5
# Fri, 15 May 2020 18:08:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 15 May 2020 18:08:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06815c0e7ea17fa3aef53a4fa131a0dd6f4b6264a2de1ce61cc6b90afe99c466`  
		Last Modified: Fri, 15 May 2020 18:09:04 GMT  
		Size: 4.6 MB (4586399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fcbc0f2c60c9c614aa5a1b87864d2cd08cf82a518562a8583bb61633048032`  
		Last Modified: Fri, 15 May 2020 18:10:59 GMT  
		Size: 92.5 MB (92498585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:f350604f8ff1f16072df44c108e770c4cc5e41a1279fb189b5ab128ad0e0af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5839716512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83da214f23799f098c202fad3f6cf9e9a79093479ef94cba66b7b4f269ac8445`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:38:12 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:38:13 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:41:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:41:09 GMT
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
	-	`sha256:d5b2cb5f64256afca14de4d1725502532023fd65f35865b465bc0990c0d07b50`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba281ac7a9cfa3600fbfa7bdab01a65ab7d906d149b0fec13104876f8296f3b`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab149127654273326a295a12eeedf69b29c056dfdd5baf233ac382e4bbbebca6`  
		Last Modified: Wed, 13 May 2020 14:47:51 GMT  
		Size: 107.8 MB (107821991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6ed8e53b44d5f4ce112ae6b4e695b7e000f92e1d36bb65bf2292d57236e9ec`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:7cdea44800ff88e226fce209d8549368d1ebc8fa9898039acc31037224374ad2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1816627462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9e86d6b300eb999e649d950faa5ccf5d2f1581e460768072bbe733dc135ee7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:41:24 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:41:25 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:43:20 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:43:23 GMT
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
	-	`sha256:fe680a4c776cb2112465925d6b7226257d08a06ebc0da04742134650c859bbbb`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151bd47c808ba6f5c19ca48b0ddbecb030d7f1d5e0e3820e5ee45602e6d09ced`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d953b3686c73f5e9d4b18f17cbb162ef95376b4a45795254192395f51bbdb9`  
		Last Modified: Wed, 13 May 2020 14:48:47 GMT  
		Size: 98.3 MB (98290011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27c8807e2ecf14d960c51c9c0eb22b8fcfd3674cc8e8b8318c532d24ba29b1`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0.5`

```console
$ docker pull julia@sha256:d0266b22a886d641e6a6f12859e9664e8563ee6e0374507ea9c4ce98a9a92e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.0.5` - linux; amd64

```console
$ docker pull julia@sha256:a7451826ead241068481f97261a1bf11aadbfb6d648ef3d676f72d21e642f7d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127097997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aca8f68b7e75d1021d3e3006be77e034615061fbd2ddabaed299b0de7b1522c`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:29 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1646a867aa17c939aeaef6e8bffc93361d9dcaac7d2f990068f03508cf29bdc`  
		Last Modified: Tue, 09 Jun 2020 07:09:01 GMT  
		Size: 95.6 MB (95563158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5` - linux; arm variant v7

```console
$ docker pull julia@sha256:bcf7766e456c8930ae20370c4d6d8a91dd26bc2ed3ba04e5b0c7e9204e2d924f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113617455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f1733b78167d6463e86c3778443e64c79c907e749e43d811fbd6dd8e4a5794`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:46:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:46:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 04:46:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:46:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 04:46:40 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 04:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 04:47:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a770ebabfd69d94d99a3dd0b3c4f87b64fca5e102575312774929eff99b51c0`  
		Last Modified: Tue, 09 Jun 2020 04:48:31 GMT  
		Size: 3.8 MB (3782747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53be19b37dff2a50445d792af5d381a870ab9d160b8976d298550b9ad8393d8a`  
		Last Modified: Tue, 09 Jun 2020 04:48:58 GMT  
		Size: 87.1 MB (87128795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7c3af80ff46b504788285e0e8ca36688e943ff524bff39802090c4843694c21d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110063821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360c01ef6037038896455058397e953d50fb518d8fec38d902ab7e6beff1f42`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:19:11 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 03:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d9c9f554133e1337121107c41f70af5bd91d9e152614e6fcb3d576e4a093a`  
		Last Modified: Tue, 09 Jun 2020 03:22:58 GMT  
		Size: 79.9 MB (79890958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5` - linux; 386

```console
$ docker pull julia@sha256:8150387e08dbb9fbb3b55792afa31de3d46c8791feb3aa773b9fcdcf4d17bc60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b4e88755e4de826b4587b435b9c5bafcda02036cc90969547284ee93481c1c9`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 15 May 2020 07:07:55 GMT
ADD file:0c3b44c83914e95e4604999a86af05023cdd2b2f795e71d737e428fae4a7e0ac in / 
# Fri, 15 May 2020 07:07:56 GMT
CMD ["bash"]
# Fri, 15 May 2020 18:07:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 18:07:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 15 May 2020 18:07:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 18:07:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 15 May 2020 18:07:42 GMT
ENV JULIA_VERSION=1.0.5
# Fri, 15 May 2020 18:08:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 15 May 2020 18:08:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a5695130085a13212b02bf2645a52af5b41dd13e6dc9b29e2d7f357e1525aa48`  
		Last Modified: Fri, 15 May 2020 07:18:14 GMT  
		Size: 27.8 MB (27754922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06815c0e7ea17fa3aef53a4fa131a0dd6f4b6264a2de1ce61cc6b90afe99c466`  
		Last Modified: Fri, 15 May 2020 18:09:04 GMT  
		Size: 4.6 MB (4586399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fcbc0f2c60c9c614aa5a1b87864d2cd08cf82a518562a8583bb61633048032`  
		Last Modified: Fri, 15 May 2020 18:10:59 GMT  
		Size: 92.5 MB (92498585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:f350604f8ff1f16072df44c108e770c4cc5e41a1279fb189b5ab128ad0e0af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5839716512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83da214f23799f098c202fad3f6cf9e9a79093479ef94cba66b7b4f269ac8445`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:38:12 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:38:13 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:41:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:41:09 GMT
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
	-	`sha256:d5b2cb5f64256afca14de4d1725502532023fd65f35865b465bc0990c0d07b50`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba281ac7a9cfa3600fbfa7bdab01a65ab7d906d149b0fec13104876f8296f3b`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab149127654273326a295a12eeedf69b29c056dfdd5baf233ac382e4bbbebca6`  
		Last Modified: Wed, 13 May 2020 14:47:51 GMT  
		Size: 107.8 MB (107821991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6ed8e53b44d5f4ce112ae6b4e695b7e000f92e1d36bb65bf2292d57236e9ec`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:7cdea44800ff88e226fce209d8549368d1ebc8fa9898039acc31037224374ad2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1816627462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9e86d6b300eb999e649d950faa5ccf5d2f1581e460768072bbe733dc135ee7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:41:24 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:41:25 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:43:20 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:43:23 GMT
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
	-	`sha256:fe680a4c776cb2112465925d6b7226257d08a06ebc0da04742134650c859bbbb`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151bd47c808ba6f5c19ca48b0ddbecb030d7f1d5e0e3820e5ee45602e6d09ced`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d953b3686c73f5e9d4b18f17cbb162ef95376b4a45795254192395f51bbdb9`  
		Last Modified: Wed, 13 May 2020 14:48:47 GMT  
		Size: 98.3 MB (98290011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27c8807e2ecf14d960c51c9c0eb22b8fcfd3674cc8e8b8318c532d24ba29b1`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0.5-buster`

```console
$ docker pull julia@sha256:1ef12f734f22c8ce0ea1eb7ac76ad4750efccdab639426bc23b742d7dc817d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.0.5-buster` - linux; amd64

```console
$ docker pull julia@sha256:a7451826ead241068481f97261a1bf11aadbfb6d648ef3d676f72d21e642f7d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127097997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aca8f68b7e75d1021d3e3006be77e034615061fbd2ddabaed299b0de7b1522c`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:29 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1646a867aa17c939aeaef6e8bffc93361d9dcaac7d2f990068f03508cf29bdc`  
		Last Modified: Tue, 09 Jun 2020 07:09:01 GMT  
		Size: 95.6 MB (95563158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:bcf7766e456c8930ae20370c4d6d8a91dd26bc2ed3ba04e5b0c7e9204e2d924f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113617455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f1733b78167d6463e86c3778443e64c79c907e749e43d811fbd6dd8e4a5794`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:46:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:46:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 04:46:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:46:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 04:46:40 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 04:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 04:47:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a770ebabfd69d94d99a3dd0b3c4f87b64fca5e102575312774929eff99b51c0`  
		Last Modified: Tue, 09 Jun 2020 04:48:31 GMT  
		Size: 3.8 MB (3782747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53be19b37dff2a50445d792af5d381a870ab9d160b8976d298550b9ad8393d8a`  
		Last Modified: Tue, 09 Jun 2020 04:48:58 GMT  
		Size: 87.1 MB (87128795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7c3af80ff46b504788285e0e8ca36688e943ff524bff39802090c4843694c21d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110063821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360c01ef6037038896455058397e953d50fb518d8fec38d902ab7e6beff1f42`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:19:11 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 03:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d9c9f554133e1337121107c41f70af5bd91d9e152614e6fcb3d576e4a093a`  
		Last Modified: Tue, 09 Jun 2020 03:22:58 GMT  
		Size: 79.9 MB (79890958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5-buster` - linux; 386

```console
$ docker pull julia@sha256:7aa7e9568b953c9ccaffe8eb52a435810b12ec7c618bf4a51e2ec8501fa026d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83565a49548f7062ea1db857ff16f3c6e7fdf96ceb20de08b8a369e482d6a54`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:25:07 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:25:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a2aa78a4cc8a35e838a0fb2dd3946e5dbdddfc0faaa9bb48e79c91fac44bb1`  
		Last Modified: Tue, 09 Jun 2020 07:27:59 GMT  
		Size: 92.5 MB (92498498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0.5-stretch`

```console
$ docker pull julia@sha256:1d1179e8a4f00fbc0be84cb698ba245d2514184dcdaa63202b131e92fcba5ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.0.5-stretch` - linux; amd64

```console
$ docker pull julia@sha256:682e5049c367e9ce77c8c6ac73e0f1d475b034794b83d223d6f0135543c9c7b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150413218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb22262966d045991306f2137cc6db81138f1cc429f8d52f2955b87dbb69d99b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:20 GMT
ADD file:6e16bc9cf28c19a1fb1fb516411643e33cbd2bdb7b6c2ce2468c6583c89871a2 in / 
# Tue, 09 Jun 2020 01:23:21 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:07:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:07:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:07:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:07:04 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:07:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:81fc1918191541a2ffb6ed1cd8386ef8302aea1b0613ebc768a00e76c1f34bb9`  
		Last Modified: Tue, 09 Jun 2020 01:27:59 GMT  
		Size: 45.4 MB (45375796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17dc3b8d966e9334692ecbd157d938f22291af6a6240b5b75e96e563d4b38d`  
		Last Modified: Tue, 09 Jun 2020 07:09:09 GMT  
		Size: 9.5 MB (9463748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9570d8717321ecf40697c2e37a28b8485479a4736fe5cef19eb297f533f09edc`  
		Last Modified: Tue, 09 Jun 2020 07:09:27 GMT  
		Size: 95.6 MB (95573674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5-stretch` - linux; arm variant v7

```console
$ docker pull julia@sha256:374ff2b811737eb5ab9294481eafb7b636b7045f48f5036cf0e5acabafdf3a3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137421846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd9881c528d0592c71f952ba55430315a796bd3be8891e4561452f6fe20e635`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:47:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:47:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 04:47:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:47:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 04:47:48 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 04:48:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 04:48:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077289b19d0a12e57779938b44bde5ff0227fda7b0031d657f558d0cb9db864f`  
		Last Modified: Tue, 09 Jun 2020 04:49:05 GMT  
		Size: 8.2 MB (8181802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33041d66df794898b2114f3cbc6d672b845bb7442acc55a6ede48432f6c4ea2e`  
		Last Modified: Tue, 09 Jun 2020 04:49:32 GMT  
		Size: 87.1 MB (87137540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5-stretch` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a58f692873ce192b799fcad8b9b5e64229c6261aa2138542da1f80c79c036c83
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131502998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bc9cb721b81f121eba3a476efe0f594105739e3b3f0ee25f50378b5887228d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:20:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:20:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:20:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:20:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:20:17 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 03:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a9f2604323329a950fd4b1d6cb02b296068afef1ecaf59294098da2fdc7873`  
		Last Modified: Tue, 09 Jun 2020 03:23:07 GMT  
		Size: 8.4 MB (8433133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079cf9c89b4491c7972f38ab76fbe1e60bfa568420dabdbb618469f898543bec`  
		Last Modified: Tue, 09 Jun 2020 03:23:28 GMT  
		Size: 79.9 MB (79908942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0.5-stretch` - linux; 386

```console
$ docker pull julia@sha256:7e0488c1ef0f5b384654d968095bc1b926b6508db76513b8935b33a11fa75717
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148067477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f121edfda82016f59a591f07e9491b308fe2f4c31977efdc9bf48829a4876fa7`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:17 GMT
ADD file:6bbeeb0773b96fccb4cd5ba81dd19ec3580f8d8a3cdd3f1d6a3d2b514fbd6eb1 in / 
# Tue, 09 Jun 2020 01:42:18 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:25:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:25:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:25:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:25:48 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:26:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:26:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9e88f215fab896e3a7d1d2ce75c0d79960b236066e9033b97e76ca7f01ff2fdc`  
		Last Modified: Tue, 09 Jun 2020 01:48:12 GMT  
		Size: 46.1 MB (46094854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d44d8a76e4fc068c5ef07bdf28b68fa1d3a08b7082895b18f31fe1cbf129cfb`  
		Last Modified: Tue, 09 Jun 2020 07:28:06 GMT  
		Size: 9.5 MB (9471016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8979d3e31d9fd6c9c1fa714ff61fda1cd2981914ffeab071d82af07af944e441`  
		Last Modified: Tue, 09 Jun 2020 07:28:28 GMT  
		Size: 92.5 MB (92501607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0.5-windowsservercore-1809`

```console
$ docker pull julia@sha256:6ff8c4c015dc489d0e839c69b9c7b83f82dbfe42068b26d1057328a6e6ed3640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.0.5-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:7cdea44800ff88e226fce209d8549368d1ebc8fa9898039acc31037224374ad2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1816627462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9e86d6b300eb999e649d950faa5ccf5d2f1581e460768072bbe733dc135ee7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:41:24 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:41:25 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:43:20 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:43:23 GMT
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
	-	`sha256:fe680a4c776cb2112465925d6b7226257d08a06ebc0da04742134650c859bbbb`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151bd47c808ba6f5c19ca48b0ddbecb030d7f1d5e0e3820e5ee45602e6d09ced`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d953b3686c73f5e9d4b18f17cbb162ef95376b4a45795254192395f51bbdb9`  
		Last Modified: Wed, 13 May 2020 14:48:47 GMT  
		Size: 98.3 MB (98290011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27c8807e2ecf14d960c51c9c0eb22b8fcfd3674cc8e8b8318c532d24ba29b1`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0.5-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:45be3df60619baf223c70adfed26b3870ea3adb9caa1c001c5d931a39ea4a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.0.5-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:f350604f8ff1f16072df44c108e770c4cc5e41a1279fb189b5ab128ad0e0af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5839716512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83da214f23799f098c202fad3f6cf9e9a79093479ef94cba66b7b4f269ac8445`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:38:12 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:38:13 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:41:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:41:09 GMT
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
	-	`sha256:d5b2cb5f64256afca14de4d1725502532023fd65f35865b465bc0990c0d07b50`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba281ac7a9cfa3600fbfa7bdab01a65ab7d906d149b0fec13104876f8296f3b`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab149127654273326a295a12eeedf69b29c056dfdd5baf233ac382e4bbbebca6`  
		Last Modified: Wed, 13 May 2020 14:47:51 GMT  
		Size: 107.8 MB (107821991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6ed8e53b44d5f4ce112ae6b4e695b7e000f92e1d36bb65bf2292d57236e9ec`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0-buster`

```console
$ docker pull julia@sha256:1ef12f734f22c8ce0ea1eb7ac76ad4750efccdab639426bc23b742d7dc817d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.0-buster` - linux; amd64

```console
$ docker pull julia@sha256:a7451826ead241068481f97261a1bf11aadbfb6d648ef3d676f72d21e642f7d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127097997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aca8f68b7e75d1021d3e3006be77e034615061fbd2ddabaed299b0de7b1522c`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:29 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:06:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1646a867aa17c939aeaef6e8bffc93361d9dcaac7d2f990068f03508cf29bdc`  
		Last Modified: Tue, 09 Jun 2020 07:09:01 GMT  
		Size: 95.6 MB (95563158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0-buster` - linux; arm variant v7

```console
$ docker pull julia@sha256:bcf7766e456c8930ae20370c4d6d8a91dd26bc2ed3ba04e5b0c7e9204e2d924f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113617455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f1733b78167d6463e86c3778443e64c79c907e749e43d811fbd6dd8e4a5794`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:46:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:46:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 04:46:38 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:46:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 04:46:40 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 04:47:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 04:47:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a770ebabfd69d94d99a3dd0b3c4f87b64fca5e102575312774929eff99b51c0`  
		Last Modified: Tue, 09 Jun 2020 04:48:31 GMT  
		Size: 3.8 MB (3782747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53be19b37dff2a50445d792af5d381a870ab9d160b8976d298550b9ad8393d8a`  
		Last Modified: Tue, 09 Jun 2020 04:48:58 GMT  
		Size: 87.1 MB (87128795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:7c3af80ff46b504788285e0e8ca36688e943ff524bff39802090c4843694c21d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110063821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3360c01ef6037038896455058397e953d50fb518d8fec38d902ab7e6beff1f42`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:19:11 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 03:19:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d9c9f554133e1337121107c41f70af5bd91d9e152614e6fcb3d576e4a093a`  
		Last Modified: Tue, 09 Jun 2020 03:22:58 GMT  
		Size: 79.9 MB (79890958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0-buster` - linux; 386

```console
$ docker pull julia@sha256:7aa7e9568b953c9ccaffe8eb52a435810b12ec7c618bf4a51e2ec8501fa026d4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124839336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83565a49548f7062ea1db857ff16f3c6e7fdf96ceb20de08b8a369e482d6a54`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:25:07 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:25:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a2aa78a4cc8a35e838a0fb2dd3946e5dbdddfc0faaa9bb48e79c91fac44bb1`  
		Last Modified: Tue, 09 Jun 2020 07:27:59 GMT  
		Size: 92.5 MB (92498498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0-stretch`

```console
$ docker pull julia@sha256:1d1179e8a4f00fbc0be84cb698ba245d2514184dcdaa63202b131e92fcba5ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.0-stretch` - linux; amd64

```console
$ docker pull julia@sha256:682e5049c367e9ce77c8c6ac73e0f1d475b034794b83d223d6f0135543c9c7b1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150413218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb22262966d045991306f2137cc6db81138f1cc429f8d52f2955b87dbb69d99b`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:23:20 GMT
ADD file:6e16bc9cf28c19a1fb1fb516411643e33cbd2bdb7b6c2ce2468c6583c89871a2 in / 
# Tue, 09 Jun 2020 01:23:21 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:07:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:07:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:07:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:07:04 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:07:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:07:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:81fc1918191541a2ffb6ed1cd8386ef8302aea1b0613ebc768a00e76c1f34bb9`  
		Last Modified: Tue, 09 Jun 2020 01:27:59 GMT  
		Size: 45.4 MB (45375796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d17dc3b8d966e9334692ecbd157d938f22291af6a6240b5b75e96e563d4b38d`  
		Last Modified: Tue, 09 Jun 2020 07:09:09 GMT  
		Size: 9.5 MB (9463748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9570d8717321ecf40697c2e37a28b8485479a4736fe5cef19eb297f533f09edc`  
		Last Modified: Tue, 09 Jun 2020 07:09:27 GMT  
		Size: 95.6 MB (95573674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0-stretch` - linux; arm variant v7

```console
$ docker pull julia@sha256:374ff2b811737eb5ab9294481eafb7b636b7045f48f5036cf0e5acabafdf3a3a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137421846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd9881c528d0592c71f952ba55430315a796bd3be8891e4561452f6fe20e635`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:06:07 GMT
ADD file:c0b9ed1244ec0acfc9054c7cb80c768878e3da99740f981ba3a82bdd854305db in / 
# Tue, 09 Jun 2020 01:06:09 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:47:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:47:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 04:47:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:47:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 04:47:48 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 04:48:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 04:48:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2566ca784846d2d0d4f9105084d94d68d8ea1a82a06a76c5bcd991ce5a10cda1`  
		Last Modified: Tue, 09 Jun 2020 01:13:35 GMT  
		Size: 42.1 MB (42102504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077289b19d0a12e57779938b44bde5ff0227fda7b0031d657f558d0cb9db864f`  
		Last Modified: Tue, 09 Jun 2020 04:49:05 GMT  
		Size: 8.2 MB (8181802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33041d66df794898b2114f3cbc6d672b845bb7442acc55a6ede48432f6c4ea2e`  
		Last Modified: Tue, 09 Jun 2020 04:49:32 GMT  
		Size: 87.1 MB (87137540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0-stretch` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a58f692873ce192b799fcad8b9b5e64229c6261aa2138542da1f80c79c036c83
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131502998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bc9cb721b81f121eba3a476efe0f594105739e3b3f0ee25f50378b5887228d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:54:22 GMT
ADD file:5cbf00485aed776e940988cadfad6853c640c13635ae54fb2b00aafccfe81a73 in / 
# Tue, 09 Jun 2020 01:54:25 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:20:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:20:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:20:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:20:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:20:17 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 03:20:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4c4f692ec920eecb1f30d9ef8e50125217decc872d7ada6eeccc36c6dcb49e4d`  
		Last Modified: Tue, 09 Jun 2020 02:00:09 GMT  
		Size: 43.2 MB (43160923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a9f2604323329a950fd4b1d6cb02b296068afef1ecaf59294098da2fdc7873`  
		Last Modified: Tue, 09 Jun 2020 03:23:07 GMT  
		Size: 8.4 MB (8433133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079cf9c89b4491c7972f38ab76fbe1e60bfa568420dabdbb618469f898543bec`  
		Last Modified: Tue, 09 Jun 2020 03:23:28 GMT  
		Size: 79.9 MB (79908942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.0-stretch` - linux; 386

```console
$ docker pull julia@sha256:7e0488c1ef0f5b384654d968095bc1b926b6508db76513b8935b33a11fa75717
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148067477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f121edfda82016f59a591f07e9491b308fe2f4c31977efdc9bf48829a4876fa7`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:17 GMT
ADD file:6bbeeb0773b96fccb4cd5ba81dd19ec3580f8d8a3cdd3f1d6a3d2b514fbd6eb1 in / 
# Tue, 09 Jun 2020 01:42:18 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:25:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:25:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:25:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:25:48 GMT
ENV JULIA_VERSION=1.0.5
# Tue, 09 Jun 2020 07:26:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='9dedd613777ba6ebd8aee5796915ff50aa6188ea03ed143cb687fc2aefd76b03' ;; 		armhf) tarArch='armv7l'; dirArch='armv7l'; sha256='cfb2712765db90f0e4fa27e57a88c6d994ebcf1781f8673ebb17b5df7962d0c5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='41cea1336ed8861413bb945740e567360e26f241eb3e10b3bb0fccd25655ed28' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='67c8f31699b79df96ce95926a363cd24ffa5bb4d9a814e071b1e8c8ff33e5a8f' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:26:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:9e88f215fab896e3a7d1d2ce75c0d79960b236066e9033b97e76ca7f01ff2fdc`  
		Last Modified: Tue, 09 Jun 2020 01:48:12 GMT  
		Size: 46.1 MB (46094854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d44d8a76e4fc068c5ef07bdf28b68fa1d3a08b7082895b18f31fe1cbf129cfb`  
		Last Modified: Tue, 09 Jun 2020 07:28:06 GMT  
		Size: 9.5 MB (9471016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8979d3e31d9fd6c9c1fa714ff61fda1cd2981914ffeab071d82af07af944e441`  
		Last Modified: Tue, 09 Jun 2020 07:28:28 GMT  
		Size: 92.5 MB (92501607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0-windowsservercore-1809`

```console
$ docker pull julia@sha256:6ff8c4c015dc489d0e839c69b9c7b83f82dbfe42068b26d1057328a6e6ed3640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.0-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:7cdea44800ff88e226fce209d8549368d1ebc8fa9898039acc31037224374ad2
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1816627462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9e86d6b300eb999e649d950faa5ccf5d2f1581e460768072bbe733dc135ee7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:41:24 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:41:25 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:43:20 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:43:23 GMT
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
	-	`sha256:fe680a4c776cb2112465925d6b7226257d08a06ebc0da04742134650c859bbbb`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151bd47c808ba6f5c19ca48b0ddbecb030d7f1d5e0e3820e5ee45602e6d09ced`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d953b3686c73f5e9d4b18f17cbb162ef95376b4a45795254192395f51bbdb9`  
		Last Modified: Wed, 13 May 2020 14:48:47 GMT  
		Size: 98.3 MB (98290011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef27c8807e2ecf14d960c51c9c0eb22b8fcfd3674cc8e8b8318c532d24ba29b1`  
		Last Modified: Wed, 13 May 2020 14:48:01 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.0-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:45be3df60619baf223c70adfed26b3870ea3adb9caa1c001c5d931a39ea4a8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:f350604f8ff1f16072df44c108e770c4cc5e41a1279fb189b5ab128ad0e0af0b
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5839716512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83da214f23799f098c202fad3f6cf9e9a79093479ef94cba66b7b4f269ac8445`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 14:38:12 GMT
ENV JULIA_VERSION=1.0.5
# Wed, 13 May 2020 14:38:13 GMT
ENV JULIA_SHA256=83c04bdc264e7ab87f4e22be9f3dff8c5a62a49c8edea6a0c85f4645d4cbac7a
# Wed, 13 May 2020 14:41:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/S', 			'/D=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 14:41:09 GMT
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
	-	`sha256:d5b2cb5f64256afca14de4d1725502532023fd65f35865b465bc0990c0d07b50`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba281ac7a9cfa3600fbfa7bdab01a65ab7d906d149b0fec13104876f8296f3b`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab149127654273326a295a12eeedf69b29c056dfdd5baf233ac382e4bbbebca6`  
		Last Modified: Wed, 13 May 2020 14:47:51 GMT  
		Size: 107.8 MB (107821991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6ed8e53b44d5f4ce112ae6b4e695b7e000f92e1d36bb65bf2292d57236e9ec`  
		Last Modified: Wed, 13 May 2020 14:47:25 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4`

```console
$ docker pull julia@sha256:6577631e3afb96c562b0649eb2a22ed6b8c2269e487fe6c50fd65938fcb1f9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.4` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4.2`

```console
$ docker pull julia@sha256:6577631e3afb96c562b0649eb2a22ed6b8c2269e487fe6c50fd65938fcb1f9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.4.2` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4.2` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4.2` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4.2` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4.2` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4.2-buster`

```console
$ docker pull julia@sha256:a33574257dddc80ca95e89efea5b945cf85d03da5eefad67b116eecddff3124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.4.2-buster` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4.2-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4.2-buster` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4.2-windowsservercore-1809`

```console
$ docker pull julia@sha256:09a533b37f51ca4e36144ea1a6e1c9564a5befbeab5168da67588451c64ec0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.4.2-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4.2-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:df028056aca74e9ac04e5c014f6cb644182741aa859874ddd57d27f5b90cc8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.4.2-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4-buster`

```console
$ docker pull julia@sha256:a33574257dddc80ca95e89efea5b945cf85d03da5eefad67b116eecddff3124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.4-buster` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.4-buster` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4-windowsservercore-1809`

```console
$ docker pull julia@sha256:09a533b37f51ca4e36144ea1a6e1c9564a5befbeab5168da67588451c64ec0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.4-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.4-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:df028056aca74e9ac04e5c014f6cb644182741aa859874ddd57d27f5b90cc8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.4-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5`

```console
$ docker pull julia@sha256:599ca548430959fceeb53c000d77905a9ea42a1dce68b69981d05c7dfe4b8a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0`

```console
$ docker pull julia@sha256:599ca548430959fceeb53c000d77905a9ea42a1dce68b69981d05c7dfe4b8a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5.0` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-beta1`

```console
$ docker pull julia@sha256:599ca548430959fceeb53c000d77905a9ea42a1dce68b69981d05c7dfe4b8a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5.0-beta1` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-beta1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-beta1` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-beta1` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-beta1` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-beta1-buster`

```console
$ docker pull julia@sha256:35ab07413daab1f7b2121b419b7db3303bb401b046a7363a8892409da4c4b2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.5.0-beta1-buster` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-beta1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-beta1-buster` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-beta1-windowsservercore-1809`

```console
$ docker pull julia@sha256:a6ecdeb64c6dee9c0fda07c72d551a7627e9ebc0633d09a89cc44476062ad1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5.0-beta1-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-beta1-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:ac1e7f531b4324c178999be76f5cbb194a58fdb8946ad50e9933c725694ab915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.5.0-beta1-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-buster`

```console
$ docker pull julia@sha256:35ab07413daab1f7b2121b419b7db3303bb401b046a7363a8892409da4c4b2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.5.0-buster` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5.0-buster` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-windowsservercore-1809`

```console
$ docker pull julia@sha256:a6ecdeb64c6dee9c0fda07c72d551a7627e9ebc0633d09a89cc44476062ad1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5.0-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5.0-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:ac1e7f531b4324c178999be76f5cbb194a58fdb8946ad50e9933c725694ab915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.5.0-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-buster`

```console
$ docker pull julia@sha256:35ab07413daab1f7b2121b419b7db3303bb401b046a7363a8892409da4c4b2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.5-buster` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-buster` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-rc`

```console
$ docker pull julia@sha256:599ca548430959fceeb53c000d77905a9ea42a1dce68b69981d05c7dfe4b8a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5-rc` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-rc` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-rc` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-rc` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-rc-buster`

```console
$ docker pull julia@sha256:35ab07413daab1f7b2121b419b7db3303bb401b046a7363a8892409da4c4b2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1.5-rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.5-rc-buster` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:a6ecdeb64c6dee9c0fda07c72d551a7627e9ebc0633d09a89cc44476062ad1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5-rc-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-rc-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:ac1e7f531b4324c178999be76f5cbb194a58fdb8946ad50e9933c725694ab915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.5-rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-windowsservercore-1809`

```console
$ docker pull julia@sha256:a6ecdeb64c6dee9c0fda07c72d551a7627e9ebc0633d09a89cc44476062ad1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1.5-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.5-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:ac1e7f531b4324c178999be76f5cbb194a58fdb8946ad50e9933c725694ab915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1.5-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-buster`

```console
$ docker pull julia@sha256:a33574257dddc80ca95e89efea5b945cf85d03da5eefad67b116eecddff3124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:1-buster` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-buster` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:09a533b37f51ca4e36144ea1a6e1c9564a5befbeab5168da67588451c64ec0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:df028056aca74e9ac04e5c014f6cb644182741aa859874ddd57d27f5b90cc8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:1-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:buster`

```console
$ docker pull julia@sha256:a33574257dddc80ca95e89efea5b945cf85d03da5eefad67b116eecddff3124a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:buster` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:buster` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:latest`

```console
$ docker pull julia@sha256:6577631e3afb96c562b0649eb2a22ed6b8c2269e487fe6c50fd65938fcb1f9e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:be0bd0706844335a3b3d17c2cd0e5d1ecacea25a5f2d915bb70bfcb12be51a8c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138465117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cbe12733d0b99e1e5816d0bcb130d89bd505e11f8b52185f76275cf6cdfa0f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:06:04 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:06:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96ac3312b03b0338063570f9f66e44bd05955be618b9551d0eb48f3873c0598`  
		Last Modified: Tue, 09 Jun 2020 07:08:34 GMT  
		Size: 106.9 MB (106930278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:06b332858a37a860206b25740e90d6a0098513c9cfcdde2de332108f61827d9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119985011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ecacacdc6722f8f248de796312066d29ceded45ede700ab935517c9dd556f9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:18:29 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 03:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:19:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c96c8b9688140f3d4bc98d4ea8fed146b6780133d04a640e9a8e7971a15888`  
		Last Modified: Tue, 09 Jun 2020 03:22:22 GMT  
		Size: 89.8 MB (89812148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:c5ab4fc2b4763ed75b707c06047bbcb0940014b1931c1ccb88a2916a070f6170
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135981742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae2379ffeb579850adb48184688451a1c0aaae5cd19849e5175465b0cbd4705`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:38 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 09 Jun 2020 07:25:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='d77311be23260710e89700d0b1113eecf421d6cf31a9cebad3f6bdd606165c28' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='f124d1b9fa68c3049d4ffe2349454f8ba1753d17d6578bc6e7cb916aed7cff4a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='ce821b6671a137dc7c2ccbf40ff08471a6791ea8af80a30d6716806608e72dab' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:25:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a4c894eb4a9c6302568043997e3df962b8d5278d272d456eab3a621100a4bd`  
		Last Modified: Tue, 09 Jun 2020 07:27:28 GMT  
		Size: 103.6 MB (103640904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:rc`

```console
$ docker pull julia@sha256:599ca548430959fceeb53c000d77905a9ea42a1dce68b69981d05c7dfe4b8a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.14393.3686; amd64
	-	windows version 10.0.17763.1217; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:rc-buster`

```console
$ docker pull julia@sha256:35ab07413daab1f7b2121b419b7db3303bb401b046a7363a8892409da4c4b2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `julia:rc-buster` - linux; amd64

```console
$ docker pull julia@sha256:bda84c18e0488509ae8b7845f722379de2785d0189ac8839b010114fb61e3af1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143155806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ccf6a968185afbcd3195ea62ff08bedd71dfc1ab4fe3419d1e80783675bd7e`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:05:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:05:37 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:05:37 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:05:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:06:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a328e51dcadbf767de376c20389133c4e738baaa6c8aa8003ec4aaa36a1d8a`  
		Last Modified: Tue, 09 Jun 2020 07:07:44 GMT  
		Size: 4.4 MB (4436574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690f1f52457f51ede803cec91597019da5b93a3ab52af69df37871122a794062`  
		Last Modified: Tue, 09 Jun 2020 07:08:06 GMT  
		Size: 111.6 MB (111620967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2dde2ebf851301b9fe45706da15a0dc182d9cab336f757828607f6038066678b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123869331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5718a47264ea71349fd48a9110571105730b4bb2daaf06776cd89eae87bcdf`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:17:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 03:17:45 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:17:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 03:17:47 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 03:18:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 03:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211e91a33aba3d2ac465ef25f59f90009a477f3d82e03c22641e48f357bbbe90`  
		Last Modified: Tue, 09 Jun 2020 03:21:08 GMT  
		Size: 4.3 MB (4315159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef297ee44c57792817721c2f54423f41dfc4d7a9a1b01a2358173c7a4f069f`  
		Last Modified: Tue, 09 Jun 2020 03:21:42 GMT  
		Size: 93.7 MB (93696468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-buster` - linux; 386

```console
$ docker pull julia@sha256:f5683998e5b6dca61efbc6d8184ea81aa5c127fdf16ba64f92a66fc81e1f5482
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.0 MB (140963275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e5fc617960c4638dd1ab0a3e776f12c6bef08a55cf38c2e0c44599a0f23be9`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 07:24:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 07:24:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 09 Jun 2020 07:24:08 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 09 Jun 2020 07:24:08 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Tue, 09 Jun 2020 07:24:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='7a81c386de7b0e8f291bfbe77cbb8e1679a03d974db2093806c78a2067b97ed9' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='a125aa5f7afe91ff5733d5065c9782b468ac6be1fb9a7f41da668a2c9a69d8a0' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='b916216d2186bdef81d768ed13d144d88c25cb6690c7ffdc704aa4d947608ed3' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 09 Jun 2020 07:24:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818dbb768b4282abbb91fefaca14197eb603ec9f779f7b706ec3eb43ce1a51f1`  
		Last Modified: Tue, 09 Jun 2020 07:26:26 GMT  
		Size: 4.6 MB (4585929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e254e9a171a1064c9815e20744f67d0349cd2694ecd6dddaf0cc34ecbca3a50a`  
		Last Modified: Tue, 09 Jun 2020 07:26:54 GMT  
		Size: 108.6 MB (108622437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:a6ecdeb64c6dee9c0fda07c72d551a7627e9ebc0633d09a89cc44476062ad1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:8f63d85d43d468ecfcef57f52bb3798377dc3aa9de087e32e84c6c13fb79badc
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849187506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e479d13afd1ac4dd3b88d458141ba243909a0fd73f7f497ae0aa5f63630315f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:18:21 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:18:22 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:20:33 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:20:35 GMT
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
	-	`sha256:491695e61ded7dd095f0a6178c6b3998e33047475d0f4ecd4ee17369e525a59d`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce919005b3dfcd7d69e3060691c1a0464b4c10fc4606643097980d8b3b205a0`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30950902cc4a5f7077e9d59b8a36bdf16706fadbbadbc7d4c9aa02f7e468ba2`  
		Last Modified: Fri, 29 May 2020 00:23:09 GMT  
		Size: 130.9 MB (130850038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5a5a8955b19493e0d555d7d48b52c3532cf0832e894f8ce015f4055a8ef642`  
		Last Modified: Fri, 29 May 2020 00:22:36 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:rc-windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:ac1e7f531b4324c178999be76f5cbb194a58fdb8946ad50e9933c725694ab915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:rc-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:581c070d574d61300b1c2e83d13d65840a2a00427d11f65fdde05fc6ff194930
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5872275823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8dcc08f251fafef77d530e57291586ee7994d3c8d22d80a98855d3d0704672`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2020 00:14:23 GMT
ENV JULIA_VERSION=1.5.0-beta1
# Fri, 29 May 2020 00:14:24 GMT
ENV JULIA_SHA256=dcc36de24e93f65648c62180cb00e04b5f46b169e7cb77535f0324e4ce0dcb61
# Fri, 29 May 2020 00:18:03 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2020 00:18:05 GMT
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
	-	`sha256:b444be1c3496b37571e46d452f9d7f7a114e85eb9d8c850369c892d92a0477e8`  
		Last Modified: Fri, 29 May 2020 00:21:44 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39a3fc4cb8ac3df44e5fce06ffe547a83c9220eadb61b7f2990a2a62ef471d3`  
		Last Modified: Fri, 29 May 2020 00:21:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bf2756ca2134be57a5926ab17acc1d6a9fdf4b3cde7e5b8de24111199892c1`  
		Last Modified: Fri, 29 May 2020 00:22:19 GMT  
		Size: 140.4 MB (140381358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741d28896a7ce9259248852752ef1cfdf791218ee7d067752c9a89d5e6d6ad9b`  
		Last Modified: Fri, 29 May 2020 00:21:43 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:09a533b37f51ca4e36144ea1a6e1c9564a5befbeab5168da67588451c64ec0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull julia@sha256:129306285e6e87dd68a97576129a0b579fed2f800d2c5a872a91bc8a4d0b7774
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847599258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00417db5c2320c39dcfbf9f5cd66cf9eeb05e3b8f797ae6c9bd12dfffb820ce3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:18:24 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:18:25 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:20:26 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:20:28 GMT
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
	-	`sha256:4053b521f8e914d87da6b1bbac13522aa4bbe843457df6a09c30d993b7009f15`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216e88a7667838e059c20dc3b6c40069554d3942e22bbc1282584e60ee0ae959`  
		Last Modified: Tue, 26 May 2020 22:23:58 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f720f9835e223a61950935ac87a2ddc23b89fdf530e29d88876ba7dacb19ad31`  
		Last Modified: Tue, 26 May 2020 22:24:27 GMT  
		Size: 129.3 MB (129261805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346c19cab393f64904fe7b2a69e4f0208e50ec5e15ccdcbf38105dd64be1b6ad`  
		Last Modified: Tue, 26 May 2020 22:23:57 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2016`

```console
$ docker pull julia@sha256:df028056aca74e9ac04e5c014f6cb644182741aa859874ddd57d27f5b90cc8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `julia:windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull julia@sha256:5912ef9be0aa7b43ffdc22a994d58a9bd7e7e4f478fd8e775280d419d20fa1ec
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5870662007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871827191f05db8bc593f0ad998efa1c2e0cb0d774c91ab0c433a72db7293da`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2020 22:15:11 GMT
ENV JULIA_VERSION=1.4.2
# Tue, 26 May 2020 22:15:12 GMT
ENV JULIA_SHA256=9775aa53f711167522ff4681f055d2ed8dc8682c99c28eb88c324ac766d0aebd
# Tue, 26 May 2020 22:18:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 26 May 2020 22:18:09 GMT
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
	-	`sha256:a0bf4afd2b9d5d7f1ddcc058d9625a415b45e37a1e0063e177dcd650678c2020`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a02aea9c8f9118e1f0d51bbd0e95b7722cd7e5f1848b75e8a085937f02b9e7b`  
		Last Modified: Tue, 26 May 2020 22:21:04 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171fe1b78e22226c650326fcba0786b1d3bfffa8610b2ae95fa1005690d17e74`  
		Last Modified: Tue, 26 May 2020 22:23:40 GMT  
		Size: 138.8 MB (138767575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199fb28cde3e830f925add23d60328f94e1c4a7a1c3c8c48daddc8791873f68d`  
		Last Modified: Tue, 26 May 2020 22:21:05 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
