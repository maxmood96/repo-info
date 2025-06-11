## `julia:rc`

```console
$ docker pull julia@sha256:3487dabfd258f22ab7c6504380a29b0e57d32db15739ca942ca3b5e8f26195ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.4349; amd64
	-	windows version 10.0.20348.3807; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:877d2aeee830dfbceeabbea1158fdc4f96f4bf8c9aeeeef5c528823e2de48c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329055756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87babee9a071464afcb5162f6afa7eca56fb97c2f449aee40880ab95d1792001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec85a0e00e87c7857805ce2b674caf1d173217e99de04a2735d1f9746bb129`  
		Last Modified: Fri, 06 Jun 2025 00:04:31 GMT  
		Size: 5.7 MB (5714714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4145f603aa9e605c72c44c54eb4209d2f525abdad97973140b69e390c022cb`  
		Last Modified: Fri, 06 Jun 2025 00:04:43 GMT  
		Size: 295.1 MB (295115341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cccc0d3a70a7fdd15fe35e6eb63a347ec6a8bb2be064d8e2088921f0bc97b0`  
		Last Modified: Thu, 05 Jun 2025 22:49:59 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:c843851c8efcd7f9e5c0a3f817bfa4d57871aadb842c7b4f0c352839c86648a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2484740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148c639c10a271c07ddf2ec27a970000369b4239503107019728c15b69b7fd6d`

```dockerfile
```

-	Layers:
	-	`sha256:704616dbb39b045b928e7127f92504586805a8a01516d5696ba842a80e3edd5e`  
		Last Modified: Thu, 05 Jun 2025 23:02:47 GMT  
		Size: 2.5 MB (2467469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10050192819f3346511e56ef628cb77eaf0855785dc246c624d0a2fd4ec15282`  
		Last Modified: Thu, 05 Jun 2025 23:02:47 GMT  
		Size: 17.3 KB (17271 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:f7a23dd5c70edc07699c97791c1968886cf599af5361c055abf6e58b2b321f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350440698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79ca026ee4c94b0e3920313ba5cbce48ea7d6e64cfa8fabe80871b74d6ade8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4701a8c1de34ee5d7491236c137872c97265053798a4239300ced2c093c24c28`  
		Last Modified: Thu, 05 Jun 2025 22:40:41 GMT  
		Size: 5.5 MB (5541512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf03f13d9915d6551de4df36b5ef1b0df74f6252c6074dcf46141dad95fe2c8`  
		Last Modified: Fri, 06 Jun 2025 00:05:30 GMT  
		Size: 316.8 MB (316833533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9afb4f6047cfd951694bd2b65c1fcfc90936705559242bf89b3005dde5761e`  
		Last Modified: Thu, 05 Jun 2025 22:40:41 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:de5b740239eb37e73380f8e8cc1de962e892e58e784f711999cf5e5c444818d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2485182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08948c661144993dd80abc63d783b392af236380cfc093fcf17d5b90814108f5`

```dockerfile
```

-	Layers:
	-	`sha256:b5cd17517f1836c9d509dedf255402c8da51df25f6aa4689e470b5167cef79f8`  
		Last Modified: Thu, 05 Jun 2025 23:02:52 GMT  
		Size: 2.5 MB (2467768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e46d3dbe9cc331a37324720e55437c8b4573eff5541f84898fd4c4e64830181`  
		Last Modified: Thu, 05 Jun 2025 23:02:53 GMT  
		Size: 17.4 KB (17414 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:b82cd52606d30f74114fd462628fe6a3dc1dda0b1a833d444c9768804408c660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272293520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946b3b3be9f4d917ebd0ac3462c8e52ad564fb113a6fb3e26e1a5c65ad620d9b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df7963a4c72d120cd3cb9fced1a14031be3229190b33e59853ed42cdcbb04b8`  
		Last Modified: Thu, 05 Jun 2025 22:40:57 GMT  
		Size: 5.9 MB (5874745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd2a5abc69fa6336f4305c2abc430eb46e579d4b0e1de76865de9a3d4310700`  
		Last Modified: Fri, 06 Jun 2025 00:06:10 GMT  
		Size: 237.2 MB (237210916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b8aaa04af463232d80ee15976a213ebd90fb5c0bb74c25efc1a3c1d9a163f2`  
		Last Modified: Thu, 05 Jun 2025 22:40:57 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:5ca8b454708357225b34f378ee55cdf68d3c9e0597144305bbcffeebe76c6f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6f49335e22a950e191b23dee0543cb7a125df2e41e0af58bff0f98e078bf8d`

```dockerfile
```

-	Layers:
	-	`sha256:05c2a8644679f162ece8a085bdbb902cd416829ad249460493f44b4b979fd7b2`  
		Last Modified: Thu, 05 Jun 2025 23:02:57 GMT  
		Size: 2.5 MB (2464606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564775f46d92e6e2d630d187441e475c0bef81cb41a5a7f2fd530f0d400b7079`  
		Last Modified: Thu, 05 Jun 2025 23:02:58 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.4349; amd64

```console
$ docker pull julia@sha256:d047e152ad5b6246a85d95a07962384299c89b49a62b280e77e35e40a198026b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3765631826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cfb37e25ca9226410cc8b6119a06d2397fa517e325ede299f388ac23919e83`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:27:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:27:49 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Tue, 10 Jun 2025 21:27:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta4-win64.exe
# Tue, 10 Jun 2025 21:27:52 GMT
ENV JULIA_SHA256=29e74fb4621ffdf635999f0f9ac53c5b3bddf87eddc09dec032f049d0879b7b5
# Tue, 10 Jun 2025 21:29:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:29:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6bed097c2f9244143667e3c761424480f294776116922a47c48122f30ff75d`  
		Last Modified: Tue, 10 Jun 2025 21:32:53 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20b2ded830bc7f86db75d49c56e720b8b35f4384e08bfc3943fef70a7598cb0`  
		Last Modified: Tue, 10 Jun 2025 21:32:54 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8d2531e27bf30460e89b16306b11ded50749496abf8d5660c3cbde0c51a7fc`  
		Last Modified: Tue, 10 Jun 2025 21:32:54 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa24fc7b0a6e5cbe01648db67b8b5caf17e8bc70476c9325ea17b0273bb2da6`  
		Last Modified: Tue, 10 Jun 2025 21:32:56 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24022c2719c0f1ec15659d8a64e6a016d24e6d5872ed076be5a4b4d6b044081d`  
		Last Modified: Tue, 10 Jun 2025 23:04:39 GMT  
		Size: 289.5 MB (289451102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f128253d0d5ccb529ae1857801adff6bdf58aef107c5b1ca82674f4b4033e04e`  
		Last Modified: Tue, 10 Jun 2025 21:32:56 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.3807; amd64

```console
$ docker pull julia@sha256:b499801cc75fc27eb482b96b86e33ad030b2baaba581b4d22e8346e8bcc5376b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2569609679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fb53ff269149e1f788d69e45b6e98f14e8d10e6805e77309df7cf82dbbe44e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:32:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:32:01 GMT
ENV JULIA_VERSION=1.12.0-beta4
# Tue, 10 Jun 2025 21:32:01 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta4-win64.exe
# Tue, 10 Jun 2025 21:32:02 GMT
ENV JULIA_SHA256=29e74fb4621ffdf635999f0f9ac53c5b3bddf87eddc09dec032f049d0879b7b5
# Tue, 10 Jun 2025 21:33:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Jun 2025 21:33:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bbcbe5d40fd64f41acfda37bd1f2824404c5dfbfef4dffb229a0cc29c0a37d`  
		Last Modified: Tue, 10 Jun 2025 21:34:51 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21352ab81ebb461c05d10bbb213e6cf2deb57606553b5f449b6e7f6bf5935ac`  
		Last Modified: Tue, 10 Jun 2025 21:34:51 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4731cc48f0fd8c2743c8e23689703a5e2d41b2fab7d1de253c71af3b0ae098b7`  
		Last Modified: Tue, 10 Jun 2025 21:34:52 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576802fb4e4d02aa62affb25c3b25e1e38c5dc011a881c6e0e89c53175ff0220`  
		Last Modified: Tue, 10 Jun 2025 21:34:52 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419e5f6874786e44f616154dca54ac435285025c4d94b64ca1ccc6701fc0b1ac`  
		Last Modified: Tue, 10 Jun 2025 23:03:33 GMT  
		Size: 289.4 MB (289351691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be6a51974b4e7ef3eb648c864086ff1c164e5bc52887932075b7b9cf88ea9be`  
		Last Modified: Tue, 10 Jun 2025 21:34:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
