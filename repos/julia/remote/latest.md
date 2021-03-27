## `julia:latest`

```console
$ docker pull julia@sha256:3d59e85518f8d6de1dc273b19f893835e2c3572de6db06ef6144bf3cb15b780d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	windows version 10.0.17763.1817; amd64
	-	windows version 10.0.14393.4283; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:39c3f721aa5ede195965e7f20575b1ee5949bdd2b42204e227d98114bcc94b83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144692197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da436e628f20142ee7f2f9eeb35b7297268af464c08f7d886cc1a430a9966e72`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:09:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:09:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 12 Mar 2021 11:09:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 11:09:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 15 Mar 2021 19:20:31 GMT
ENV JULIA_VERSION=1.5.4
# Mon, 15 Mar 2021 19:20:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='80dec351d1a593e8ad152636971a48d0c81bfcfab92c87f3604663616f1e8bc5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='7ffdf6358d6c2b8a53757e517998d55833c363d4730c9452ddd44b223f10333a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='70f7327a26dd2dda87eb6cdf99269f974ae722a02c54b2faa174ceda125bf006' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='4a0ae1b0c3bec1836067ce17b2eab2106f881f18a60f833f6272092f96e86fe7' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 15 Mar 2021 19:20:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fec5d00e162f64cdb9c8caca9ca84941b470a7c485ed4e5c11451399705edb`  
		Last Modified: Fri, 12 Mar 2021 11:13:35 GMT  
		Size: 4.5 MB (4457038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f314bbc0ad4b18485974c4f6053a1fa2758f1c60e850a6dddd649dda19345b`  
		Last Modified: Mon, 15 Mar 2021 19:23:54 GMT  
		Size: 113.1 MB (113134158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:784e1c28ac05803e79bf0796a25e0a4b7efaf77345c84304703f402ef1fcc349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135629984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80e5e8d920c0f8e8da516e391ed3839d4d6568e9d9196fe4c793fb4c0025fdf`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:53 GMT
ADD file:6130ddc0a939dd72c0614de4aa77de47aa16fe211274bacb31995aa1a0526164 in / 
# Fri, 12 Mar 2021 01:53:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 18:52:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 18:52:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 12 Mar 2021 18:52:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 18:52:56 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 15 Mar 2021 21:59:48 GMT
ENV JULIA_VERSION=1.5.4
# Mon, 15 Mar 2021 22:00:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='80dec351d1a593e8ad152636971a48d0c81bfcfab92c87f3604663616f1e8bc5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='7ffdf6358d6c2b8a53757e517998d55833c363d4730c9452ddd44b223f10333a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='70f7327a26dd2dda87eb6cdf99269f974ae722a02c54b2faa174ceda125bf006' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='4a0ae1b0c3bec1836067ce17b2eab2106f881f18a60f833f6272092f96e86fe7' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 15 Mar 2021 22:00:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:706ee5d0a6b53d9257cbea22d8409fb22c867ab3a001c65f6b8bfd37dace0e58`  
		Last Modified: Fri, 12 Mar 2021 02:01:39 GMT  
		Size: 25.9 MB (25856512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1b27552a8270c637784c4f893543b3e7155897fd499452d663a15f41a754c0`  
		Last Modified: Fri, 12 Mar 2021 18:56:20 GMT  
		Size: 4.3 MB (4337861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fa9ec637c0936a2fcf9b9e85873125201b01dff099e0385bc6edc5b46d968e`  
		Last Modified: Mon, 15 Mar 2021 22:02:10 GMT  
		Size: 105.4 MB (105435611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:7e3837584849d8951e5bfa96d6ae2aa7a5369f5a036f1b05d492b0e417d85cee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151164793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bbef63a58ea848f755994889a049c377dd174e43b26a3f99f6738ce9230dd6`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 26 Mar 2021 13:53:11 GMT
ADD file:6c7524352aadfb597840d7c62001b10cf663f17dc2752a1bc5ad40b538138432 in / 
# Fri, 26 Mar 2021 13:53:12 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 23:57:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 23:57:21 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 26 Mar 2021 23:57:21 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 23:57:21 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 26 Mar 2021 23:57:21 GMT
ENV JULIA_VERSION=1.6.0
# Fri, 26 Mar 2021 23:57:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='463b71dc70ca7094c0e0fd6d55d130051a7901e8dec5eb44d6002c57d1bd8585' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='0f496972d26cea88151204d03e6bd87702aa1ff983de3b1e4f320c48ef67325f' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='601fea2ece89df4398146d077ee456a9abe0c9d2f19c5fc22be1f01c77949777' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='594639c9824f8dfb26074e875b27d7ed6c354d77a89469acbbe03e819021cb57' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Fri, 26 Mar 2021 23:57:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8cd20c3ac698e839ccd9bbdb86bc90efa00779d975e4064809852f86f56d8f3e`  
		Last Modified: Fri, 26 Mar 2021 14:01:40 GMT  
		Size: 27.8 MB (27760999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bba61a9111ef91abdb7108a50022a3164eb5ca2c7bb9e3a263a7b82c922b7a`  
		Last Modified: Fri, 26 Mar 2021 23:59:58 GMT  
		Size: 4.6 MB (4610340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18c62d46178edc7f83710c22102e5a8ce4c91a7c74dcb123ceb009b4849a47a`  
		Last Modified: Sat, 27 Mar 2021 00:00:22 GMT  
		Size: 118.8 MB (118793454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - linux; ppc64le

```console
$ docker pull julia@sha256:56029200203d413d55fc513d260c57a11dd8e1465a8960322a35e07dfe577216
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132972500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0719be03137261bc544c7de2ae7901d622ee4ff2d452d8ffa2f3150e329eb3`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 05:36:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 05:36:12 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 12 Mar 2021 05:36:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 05:36:27 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 15 Mar 2021 19:26:26 GMT
ENV JULIA_VERSION=1.5.4
# Mon, 15 Mar 2021 19:28:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) tarArch='x86_64'; dirArch='x64'; sha256='80dec351d1a593e8ad152636971a48d0c81bfcfab92c87f3604663616f1e8bc5' ;; 		arm64) tarArch='aarch64'; dirArch='aarch64'; sha256='7ffdf6358d6c2b8a53757e517998d55833c363d4730c9452ddd44b223f10333a' ;; 		i386) tarArch='i686'; dirArch='x86'; sha256='70f7327a26dd2dda87eb6cdf99269f974ae722a02c54b2faa174ceda125bf006' ;; 		ppc64el) tarArch='ppc64le'; dirArch='ppc64le'; sha256='4a0ae1b0c3bec1836067ce17b2eab2106f881f18a60f833f6272092f96e86fe7' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding Julia binary release"; exit 1 ;; 	esac; 		folder="$(echo "$JULIA_VERSION" | cut -d. -f1-2)"; 	curl -fL -o julia.tar.gz.asc "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz.asc"; 	curl -fL -o julia.tar.gz     "https://julialang-s3.julialang.org/bin/linux/${dirArch}/${folder}/julia-${JULIA_VERSION}-linux-${tarArch}.tar.gz"; 		echo "${sha256} *julia.tar.gz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Mon, 15 Mar 2021 19:29:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfdf7459a9ef48e385530406312674264e988d68c206d2c12364c9f4f5a2d71`  
		Last Modified: Fri, 12 Mar 2021 05:40:27 GMT  
		Size: 4.9 MB (4853438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b12154129415ecf0e4c8cb5af3c8683b87fdf9000fc362769f977e1563cfe8`  
		Last Modified: Mon, 15 Mar 2021 19:30:52 GMT  
		Size: 97.6 MB (97593334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.17763.1817; amd64

```console
$ docker pull julia@sha256:dcce8bb6fc5c651b5a25f7e3b02f32ff8614632fbbb6ab6ba8ea91104e9e08b4
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2603924024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c65e25dff743723213e408ace787acae99efdbf5bb638235a7ae12a721c824`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Mar 2021 21:15:17 GMT
ENV JULIA_VERSION=1.6.0
# Fri, 26 Mar 2021 21:15:18 GMT
ENV JULIA_SHA256=0c1f5cfe5d4ffb3505282a46169d85f31666217d3ada4831a4a5d7f2b981f0cc
# Fri, 26 Mar 2021 21:17:14 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 26 Mar 2021 21:17:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2143539f8c15bee79cabd7fd9c05c742ff15fb18376d203b1a830432d9868bc1`  
		Last Modified: Fri, 26 Mar 2021 21:21:18 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cba3cdd067d8315ce9c637fba44a9a58ae3838c03290ab5c186ba32cf7b4a1f`  
		Last Modified: Fri, 26 Mar 2021 21:21:18 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ff8e023ad9b9306e9ada240634da3cfdb8a8d9c3a68f500e6dc8203e842592`  
		Last Modified: Fri, 26 Mar 2021 21:24:11 GMT  
		Size: 142.4 MB (142383851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0610ba4a9aa0473c3652595f1833f8f4b529f16c5d9a3448612bee3a6b368318`  
		Last Modified: Fri, 26 Mar 2021 21:21:19 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.14393.4283; amd64

```console
$ docker pull julia@sha256:59da4d4967c74fe47cfe321d74af5ef6423073e84c44830a60e39900370a9195
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5940060606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5a3cc08f6a8060d830f9f03755f9eac7c475b943e34065fa3216a69db86ccc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Mar 2021 21:17:30 GMT
ENV JULIA_VERSION=1.6.0
# Fri, 26 Mar 2021 21:17:31 GMT
ENV JULIA_SHA256=0c1f5cfe5d4ffb3505282a46169d85f31666217d3ada4831a4a5d7f2b981f0cc
# Fri, 26 Mar 2021 21:20:07 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Fri, 26 Mar 2021 21:20:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0edb3570533a69186e50a702d262267c9346be7ae9fa5e6f7235038f108d62ba`  
		Last Modified: Fri, 26 Mar 2021 21:24:27 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ab1f5117a07e788841f85a011c30d04edf17a7bc9c128f43c5fedff2c3843`  
		Last Modified: Fri, 26 Mar 2021 21:24:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bb254acd83ec4913b93e058a70cd0535df97a0ba7c67ac8efd73e7ff919014`  
		Last Modified: Fri, 26 Mar 2021 21:24:58 GMT  
		Size: 143.1 MB (143144216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6dd83fe9334b5db7078886cf406800bc0887f8486c4674ae04c76157c0d65e`  
		Last Modified: Fri, 26 Mar 2021 21:24:28 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
