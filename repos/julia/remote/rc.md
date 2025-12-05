## `julia:rc`

```console
$ docker pull julia@sha256:49ce8bf1cf8d645fe053fc10adc09d254f37ee6ff6fde6a0622781edce094252
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:b1ad431dc54671c80dd6021ff8368791ba000eb89368055623b512917c70c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342734146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40f65e6b419d06a905648f0a26903620a0c76b4b929302930b3579b04417e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 19:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 19:02:55 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Dec 2025 19:02:55 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 19:02:55 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Dec 2025 19:02:55 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 02 Dec 2025 19:02:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 02 Dec 2025 19:02:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 19:02:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 19:02:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed77eb6c4533000cf719f7c704b57ebfb9fac2d89e96449375634221efddded`  
		Last Modified: Tue, 02 Dec 2025 19:04:21 GMT  
		Size: 6.2 MB (6242920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac28fea8aa292bb1adcf4a9c64780ffe9a2cec762598f3406dfd1b7a0d78c0dc`  
		Last Modified: Tue, 02 Dec 2025 21:10:54 GMT  
		Size: 306.7 MB (306714371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5434f79ff78b3e88adb493e2398f04c0d5ae767e3f462ff82df5b540b3811617`  
		Last Modified: Tue, 02 Dec 2025 19:04:21 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:2cd7cbd675abc671a1491ce3b2ba9df9e3313d596324b89898ffe567452ce923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba919f2c40d2d14da929e56338aef83d0ade7695f99a5e0e5fc3dbc579757ec0`

```dockerfile
```

-	Layers:
	-	`sha256:33393d931a0076dd2af69ff9b83ffcb4b55d2c981712de762b3c2753c2f9a16f`  
		Last Modified: Tue, 02 Dec 2025 21:03:06 GMT  
		Size: 2.2 MB (2240783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc5b88869ba3cea82e3b6b01890249fd25dc976cfd5ea5809e8ac55de590b433`  
		Last Modified: Tue, 02 Dec 2025 21:03:07 GMT  
		Size: 17.2 KB (17218 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1a5d41eaed96bb512dc44ddc62f1b466d9891f4bb63cfc590519f97d0482f5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366004469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461aed287037345bfabec32ba3531f1ef3f7980aa0d171033393ca66d28a7fd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 19:02:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 19:03:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Dec 2025 19:03:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 19:03:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Dec 2025 19:03:09 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 02 Dec 2025 19:03:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 02 Dec 2025 19:03:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 19:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 19:03:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c096c5d260a6febb2a8f798e5a7eb9496de1e4fe2065c73ecf2fb7760f8b20b`  
		Last Modified: Tue, 02 Dec 2025 19:04:37 GMT  
		Size: 6.2 MB (6153443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b530b19acaa36a20d4bf8782ece58c1f595f2d70fa4c2c213c636ff923ad7b62`  
		Last Modified: Tue, 02 Dec 2025 20:00:00 GMT  
		Size: 329.7 MB (329712047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd04354eeb1b1dc02287be5baaf827bb14f1769641604b785c44a8d5bfad41b`  
		Last Modified: Tue, 02 Dec 2025 19:04:36 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:c0a2e249a2a9a0471ab85502e818abb26f232573823f1b396daebf6a9bb719cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d41bfa05470e7e4fa20df40c69b143d3996f1ab939035c35888ecc2a9af347`

```dockerfile
```

-	Layers:
	-	`sha256:557cbfbbffcda8e1e1a328d7ed3266293ef12a72d376de2d1b0c87fd05625ceb`  
		Last Modified: Tue, 02 Dec 2025 21:03:11 GMT  
		Size: 2.2 MB (2241091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e834924ae580773ac9c60d707f73a19569769dba3c61c02877994da2b69f3ef`  
		Last Modified: Tue, 02 Dec 2025 21:03:12 GMT  
		Size: 17.4 KB (17363 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:276e5543eafb825c3e8afad52b87018150d8c01172e1539297198798c071926a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280240725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8a65ebe40c8c733f486bd11f0a6e8cb4347581edcb13d6249f6d547bef5338`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 02 Dec 2025 19:02:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 19:02:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Dec 2025 19:02:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 19:02:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Dec 2025 19:02:46 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 02 Dec 2025 19:02:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-alpha2-linux-x86_64.tar.gz'; 			sha256='987aa3aad11e0b5c078dfdee7f8d54eeabdc10bcddd245bda18e28ab4de6119d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-alpha2-linux-aarch64.tar.gz'; 			sha256='c558a08f69d1984096d0bac825148cba2dd6b2eea3c5a3d8a5def2cd718af196'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-alpha2-linux-i686.tar.gz'; 			sha256='15b15af06b603efa0523e2f1b19cacaefcddda13595906c276ddec0b3194c0b2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 02 Dec 2025 19:02:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 19:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 19:02:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a04565e0def9479d44f401fdcc4ba5d8e9adb3bf850c762a296e9cdaf5a985b`  
		Last Modified: Tue, 02 Dec 2025 19:03:38 GMT  
		Size: 6.4 MB (6427615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff59ebf4b491cf0b6113cf3931a97ea142fb23c10bec00d86512391609e0791`  
		Last Modified: Thu, 04 Dec 2025 22:07:33 GMT  
		Size: 242.5 MB (242519670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d2f754d56f0bb3b5b8ceae231853805f7676ff57b71a4f6385287a42044db`  
		Last Modified: Tue, 02 Dec 2025 19:03:34 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:d5dfa449691e1318ecbe45f11c39bea2cd26a7e96a8d5e84792e04c1a4b2bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e170491d6af6a4f9a397590330b6f9b4be708e5bd0f0949203a6b040fb29f190`

```dockerfile
```

-	Layers:
	-	`sha256:d6da31f347a6a2aae44e487a37e7972601281c47f15ce8e37bc370d7e1eda165`  
		Last Modified: Tue, 02 Dec 2025 21:03:26 GMT  
		Size: 2.2 MB (2237918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c127051fad803704a6123d9310567e1f6be6eb3e61806ce9f3eeaa3c01846343`  
		Last Modified: Tue, 02 Dec 2025 21:03:27 GMT  
		Size: 17.2 KB (17176 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:710c5d609bc83bb05746cae905def34f1e9ff8d83ff4f83a8adda4b9f35001c0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3545626674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb390f2895272452331b1b1d20010368e5385cac0eb7813535828ddf50f09dff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 19:01:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 19:01:22 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 02 Dec 2025 19:01:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-alpha2-win64.exe
# Tue, 02 Dec 2025 19:01:24 GMT
ENV JULIA_SHA256=ec84bd651c739436b2ab397f4a156ed269030f277d075031104eecbf6904079a
# Tue, 02 Dec 2025 19:03:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 02 Dec 2025 19:03:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8141b58e228ac47c42461930c677cd23e8e308c83fed29a5847b300cc7b1e828`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f4cd6912772159706904dabb489e9f38f4fcbdc4ff08bfaec1c0d6fd3ac3d4`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdde5cf68e32bec7badd008412379831c34f31083a038f8d79aafb23d6d121c`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88ed419ff80e5f510f8953c401d8c9d63ac2734d43c164fab3d9475f01457d9`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff8814e2bdc25e8c91396e45b0d6c3af22d179237537ed881bc9fdacd45ffb`  
		Last Modified: Tue, 02 Dec 2025 21:03:26 GMT  
		Size: 310.2 MB (310164340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa8fe5a9bde1fcf9fcb2c9164dbf68054c011dc27998fa5b7cfb5d46dd5d5ce`  
		Last Modified: Tue, 02 Dec 2025 19:10:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:519e48a55bc407b996f09d36239a951a05431a38adb3f2087db9169e3cff3ef3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2080208074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05afcf743302ea7ea3d6f9acacdef6a80a5b276c9c67e9b064b06ed36b62bd9`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 19:25:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 19:25:02 GMT
ENV JULIA_VERSION=1.13.0-alpha2
# Tue, 02 Dec 2025 19:25:03 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-alpha2-win64.exe
# Tue, 02 Dec 2025 19:25:04 GMT
ENV JULIA_SHA256=ec84bd651c739436b2ab397f4a156ed269030f277d075031104eecbf6904079a
# Tue, 02 Dec 2025 19:27:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 02 Dec 2025 19:27:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac818d0c144bc3aaf6252b57c479b05a7e19f744bdbab4f72d9af5e82709cbc`  
		Last Modified: Tue, 02 Dec 2025 19:33:39 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445a6a87b11d96e720bbbb7fef8657ccde2449cb91a7c8baf018ad5bf5989e7f`  
		Last Modified: Tue, 02 Dec 2025 19:33:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cfbcfb712e96326db31e4152f681ec613bacd2181f445e403e1d80bae0bf63`  
		Last Modified: Tue, 02 Dec 2025 19:33:39 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97cb4f0c30c9a48218aeb70c7e3335d48a2af09d084ef0209047698771275510`  
		Last Modified: Tue, 02 Dec 2025 19:33:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90566bf1741c45ab9afa8cf3350d4e286ab6de4655a52472c8ee50ba83f7f203`  
		Last Modified: Tue, 02 Dec 2025 20:10:30 GMT  
		Size: 310.2 MB (310240015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914b83696e9fed0a33e5263c691f48a80cef4bbb5b86775f5e71549b0eb67a69`  
		Last Modified: Tue, 02 Dec 2025 19:33:39 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
