## `julia:rc`

```console
$ docker pull julia@sha256:31a4e5eeed2293f1280fab2f8acf612826c9041298ba2349426e6fc0e74c485e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.4652; amd64
	-	windows version 10.0.20348.3932; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:c68d83fe08d65f58f41f27985d5825e40f263778d20faeac887da9f6ae18b29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329060441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4627819d198a44624543d3e9ab6618fac135c43167aef69de42a410eddba5ef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8590f986ae21e2e9795c08890a4492e3904bbf841bd47094277bf1136e0eb2fc`  
		Last Modified: Tue, 01 Jul 2025 06:09:19 GMT  
		Size: 5.7 MB (5714659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11b81035f26d9b330dbe106748f379a3850321197f4c0bb84ba3b38cd2b59b`  
		Last Modified: Tue, 01 Jul 2025 06:09:35 GMT  
		Size: 295.1 MB (295115269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc869335ca62b80b3bcd73d7fd7b9c617ec85459cfb6ebf85cedfd52d28f9ff8`  
		Last Modified: Tue, 01 Jul 2025 03:40:18 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:c14af96d17cf9eaf782c74d998f8567e9f5ef11dcdb2014ea1769488456c7686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba643ca08417feafb7c01a244f1e890dd25167ee4c8433fdc1c566e26e0aedd`

```dockerfile
```

-	Layers:
	-	`sha256:d9da18a47069d02315d1cf0aece1f7fd44b85e4c24920453c84a4c138be8f996`  
		Last Modified: Tue, 01 Jul 2025 05:03:46 GMT  
		Size: 2.6 MB (2566185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c860ce9975be20397122623491a8cdfbf33174f284fb1c677cda5de70d1447d6`  
		Last Modified: Tue, 01 Jul 2025 05:03:46 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:860ca58620baf238ebce15a98c102a049ce451fdbfab040ce3f9b61a7058c498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350462946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0d28714d3bd662232cf82021c304c23ab6451332b46d9c8217ddba0a15497c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa97968f2bc597e072a5a009583a3f4821ec3debbf5159be82b39633a0c8e217`  
		Last Modified: Tue, 01 Jul 2025 03:00:42 GMT  
		Size: 5.6 MB (5551316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c05b31f4576ff20ae1295fb2852a009089bb6c502123f80e74d267baef6004`  
		Last Modified: Tue, 01 Jul 2025 05:35:54 GMT  
		Size: 316.8 MB (316833581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d72723e2539346d7e999cbb486cb88e929119c76e2519330bc6feaccc15d75`  
		Last Modified: Tue, 01 Jul 2025 03:00:41 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:81260c4b98ee9281a60e02a90c8b0fa1b3cb87741dbca33f63745b50dbf02db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe204d4fb5d8fb9b9d906042b4f40463f52435b8529962f6f3f77e58f3531a6c`

```dockerfile
```

-	Layers:
	-	`sha256:44885595d799994f61c8e9179f685d79afd6bfbf7d51ab8f1f5897f97f8c7750`  
		Last Modified: Tue, 01 Jul 2025 05:03:51 GMT  
		Size: 2.6 MB (2566484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184870a2817953e762179a8466b090a83bcfa0736c644020d6d0185eba049add`  
		Last Modified: Tue, 01 Jul 2025 05:03:52 GMT  
		Size: 17.4 KB (17414 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:b9be67bc8ce69e131594e23819ba8a7e615e5e82f972eb46cd4a67e45e13e44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272299993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2325a559e581e1272d916e091ffbd09874c980172caa3573bdb3f55c490630d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Thu, 05 Jun 2025 17:59:29 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Thu, 05 Jun 2025 17:59:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Thu, 05 Jun 2025 17:59:29 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Thu, 05 Jun 2025 17:59:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta4-linux-x86_64.tar.gz'; 			sha256='cead6a6ff3464af359258579a3ff6fb1d6f65aa93cb7b32b00691c23752f1cd7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta4-linux-aarch64.tar.gz'; 			sha256='e8ae058e3534a979de94688786f546060bbc676ac06035cd4350fbc53a1ddc21'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta4-linux-i686.tar.gz'; 			sha256='748eabeb5a31b9eb096b641010d1a0a9bf63283f58425734660c1056ba790e55'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Jun 2025 17:59:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Jun 2025 17:59:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2df16a6f911bec0b9a672aaa2bdb717ef4a40c65b87c80c37e04be6a7c3d9fc`  
		Last Modified: Tue, 01 Jul 2025 02:13:23 GMT  
		Size: 5.9 MB (5876305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac24f584a33a76265c4f9c3b42176d0a9237f17e5c42220e6aa223d1ac2f4da0`  
		Last Modified: Tue, 01 Jul 2025 13:22:47 GMT  
		Size: 237.2 MB (237210884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0fd4fe597ef2baaec75998eebb7611268fd2dd735ff4364824f29f3b5824f7`  
		Last Modified: Tue, 01 Jul 2025 02:13:22 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:21ed26f23c068af82df63522843e9c82e597b0435a173d5d79df74bf9d234a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f7d0c0d70b3a43da6a4233644616476d8af24251ffdbb801876c6d0aeb6f5f`

```dockerfile
```

-	Layers:
	-	`sha256:5f3939f36577699e4324de99b3576d04953f3a205bb50a45e5361cfad04cc648`  
		Last Modified: Tue, 01 Jul 2025 05:03:56 GMT  
		Size: 2.6 MB (2563322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca35c50fc44a9a40132ab83bc74863c852b418a806b8f321662cb5e439762506`  
		Last Modified: Tue, 01 Jul 2025 05:03:56 GMT  
		Size: 17.2 KB (17225 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.4652; amd64

```console
$ docker pull julia@sha256:1b7f160b1aa29cd4c925558c8d2547f6a60442ca23c758753326289d524ca0a9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3780604873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f200700d6874215f0a0917c9bf315f725939733537d18b722b030c2b24ade1a6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:09:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:13 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Wed, 09 Jul 2025 18:09:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta4-win64.exe
# Wed, 09 Jul 2025 18:09:16 GMT
ENV JULIA_SHA256=29e74fb4621ffdf635999f0f9ac53c5b3bddf87eddc09dec032f049d0879b7b5
# Wed, 09 Jul 2025 18:10:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:10:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628109526f968ba4fbd86e95a181f27288bce2f5a8cd5789a052e518e1008b06`  
		Last Modified: Wed, 09 Jul 2025 20:03:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f67fac0433c25f901e977c1e09d6688840b1fbed4b9f66df1fec954254af52`  
		Last Modified: Wed, 09 Jul 2025 20:03:14 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d1fff3ead93dc07f292578a5ca9d43b8bfb5eff93b9346c5d2f15bb62f637d`  
		Last Modified: Wed, 09 Jul 2025 20:03:14 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e34f2c407ad0dcbe077dd1ab845b033e2dd50e6da38f40ebe788abe368189e7`  
		Last Modified: Wed, 09 Jul 2025 20:03:14 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5291184aa67e7c61e5ce86578b84e03c265fcc53076bb2ae83df758dbd18853`  
		Last Modified: Wed, 09 Jul 2025 20:04:09 GMT  
		Size: 289.4 MB (289424938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f00d25b78ff411e2e8cb3f8a6e0b7f47da1338e463681645a42d0b64ee8d7`  
		Last Modified: Wed, 09 Jul 2025 20:03:15 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.3932; amd64

```console
$ docker pull julia@sha256:6784a75f80dae47f09b2c8a323bdeea20bac5538556b464db5832776ef22800d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2569943184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328975e06991be208dcb7e8fbde7c262364c8ea4ca7c3b987934939e87846bf5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:06:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:06:41 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Wed, 09 Jul 2025 18:06:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta4-win64.exe
# Wed, 09 Jul 2025 18:06:43 GMT
ENV JULIA_SHA256=29e74fb4621ffdf635999f0f9ac53c5b3bddf87eddc09dec032f049d0879b7b5
# Wed, 09 Jul 2025 18:08:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:08:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea818ad43134ab9aa9a94ef0a632ee8e0a158a1bc47ded911db12faf3ccd8ad`  
		Last Modified: Wed, 09 Jul 2025 20:03:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b823e48551f68303240d75bfc2c445f3ea84de2ef8033f66fb5e4ad09ab40fcc`  
		Last Modified: Wed, 09 Jul 2025 20:03:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8396c66218321f77da41b87b7d8d9773924c4c99ef41d0962abcbf4cb1beb2`  
		Last Modified: Wed, 09 Jul 2025 20:03:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787ee83779814aec0ed6a0e6f0144082ca7a6004fd8aa723ac66563d55e8a134`  
		Last Modified: Wed, 09 Jul 2025 20:03:16 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36953ddfc9dcd69a4b5f7336502d4adc44578c91b5b1b36dd98b6f01fe912632`  
		Last Modified: Wed, 09 Jul 2025 20:03:43 GMT  
		Size: 289.3 MB (289333274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a964a913be9e25b59cb64b11922597d8bf52706986de1310c6cc30cc9fb3896f`  
		Last Modified: Wed, 09 Jul 2025 20:03:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
