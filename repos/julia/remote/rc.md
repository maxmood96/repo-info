## `julia:rc`

```console
$ docker pull julia@sha256:cdf6460c56929925c15b8b4c8784a5d4eff3847d751cd6719076d00ee0cd7efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:57492c8f2a161c33935c11d7cfe3800843e7eadb196c48c919bda0cfb8135aa4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180885032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f3cb743ebea2a42462f72a606d4a571752bc0109a27d29f0a9604eab80aa5c`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:38:15 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 04:38:15 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 04:38:15 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Aug 2022 04:38:15 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Tue, 02 Aug 2022 04:38:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 02 Aug 2022 04:38:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654fce16cc037ef8e49e9de0d93725a4c38623de2c39f225b0bdc609b3bf8743`  
		Last Modified: Tue, 02 Aug 2022 04:41:24 GMT  
		Size: 2.4 MB (2426463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719e99e0be6c930f3ea263b7ff4d190cff7fbd35ba6f84eca04c19902ec4fe72`  
		Last Modified: Tue, 02 Aug 2022 04:41:47 GMT  
		Size: 147.1 MB (147091812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:d7fabc4545fd3213a25fb55fa0ae7a65595723586de5ae601d6b3cc719b70ba5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.2 MB (173196241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9138302989fe8e44c97ec30b1534ead459b5bff4dffd87a4718e6b312372995f`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 00:40:38 GMT
ADD file:6039adfbca55ed34a719c37672c664e3524130a0e2a3b8663629b8120b81b790 in / 
# Tue, 02 Aug 2022 00:40:39 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 03:49:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 03:49:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 03:49:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 03:49:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Aug 2022 03:49:04 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Tue, 02 Aug 2022 03:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 02 Aug 2022 03:49:27 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a9fe95647e78b5516c7e2327355b6996e2ea295cd76ae242cbfe87f016b4e760`  
		Last Modified: Tue, 02 Aug 2022 00:46:05 GMT  
		Size: 30.1 MB (30054304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8642deeb25c491828f0c5aea294f6ea9772e6c31acc0290872b44bc353b1fdae`  
		Last Modified: Tue, 02 Aug 2022 03:52:25 GMT  
		Size: 2.4 MB (2413549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257c04260ef618b4b5157ebb402596afa57537704ac75d78234028480109ba16`  
		Last Modified: Tue, 02 Aug 2022 03:52:45 GMT  
		Size: 140.7 MB (140728388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:e7100d150bd6b5d5f941b7ab1afe766785dafe796737743054741c360d9fef45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178968466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64e743b6c2608c5a934ff2824ac966d699da0e8d988cc2e4797f681a96c378d`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 02 Aug 2022 00:39:20 GMT
ADD file:f771e2286465694126158821089d801c7296376be2a56189e6041a15d2fe79f5 in / 
# Tue, 02 Aug 2022 00:39:21 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:52:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:52:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 02 Aug 2022 15:52:24 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 15:52:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 02 Aug 2022 15:52:26 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Tue, 02 Aug 2022 15:52:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.8/julia-1.8.0-rc3-linux-x86_64.tar.gz'; 			sha256='7c57ac9aabce9b3cdc0f7bb1c393fe8058b794ddbb4168fcb28800b6459aa815'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.8/julia-1.8.0-rc3-linux-aarch64.tar.gz'; 			sha256='40ae51fe3d20b27b40163daef761c2565529554bca01eb38bb19532400165586'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.8/julia-1.8.0-rc3-linux-i686.tar.gz'; 			sha256='047775e2f21facf288422ed7f60459c37b9083fadf24d2d6740fd965c7e940be'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 02 Aug 2022 15:52:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:90eb7f0ce9f33cf5dcd67d54c2fa606186dbaa5f95b6046f36145097267f9e53`  
		Last Modified: Tue, 02 Aug 2022 00:45:14 GMT  
		Size: 32.4 MB (32374054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8a517a4db3da824a60e9acbc98f3e3ee40a5449c73b14984772ccad44f5717`  
		Last Modified: Tue, 02 Aug 2022 15:56:09 GMT  
		Size: 2.5 MB (2531608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0032bb8335a4c22e7ec6935b00e48b92c36edebd9e74b779d5af87683b8776`  
		Last Modified: Tue, 02 Aug 2022 15:56:30 GMT  
		Size: 144.1 MB (144062804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.825; amd64

```console
$ docker pull julia@sha256:f69c9bf069ececc6d9b244017e78a66d56f3781f0b3a7345e2228094659c5224
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2460153604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0292a7024e1d0d6fcac924dd1fb1d0f2e91b5fe62dbda6193bcf03e4ec3e777b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Jul 2022 19:15:56 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 19:15:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.0-rc3-win64.exe
# Mon, 18 Jul 2022 19:15:58 GMT
ENV JULIA_SHA256=fd861d6c4a97f5319cbb5a4b508fc16fc3aaacbe113fa5cbe31b37fa00e4f18e
# Mon, 18 Jul 2022 19:17:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 18 Jul 2022 19:17:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e73b3b8f6da6afb1a5493041710bddf5235c0fec8dcc2ffb3e79ab2d28ba0c`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab7128d15a612012fee5edfe7c8c7e4e3ac5903c6bbcb274bd39669fd79b91e`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba394c9ef183c1f69545fad25a946eb3dd5da3f7dcecebdcd6a4e69f227cff`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33570793b612bc509b94ba4f6c7d0c6a290e1a9371dd67556de5fa3b861badb`  
		Last Modified: Mon, 18 Jul 2022 19:22:22 GMT  
		Size: 159.9 MB (159914919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19186e3b06a4dc04c883be9db2fd4d830ecc9e1515feeac10109d3edf4d5d033`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.3165; amd64

```console
$ docker pull julia@sha256:f715778ac965c4dd477b2b0fa0562904f7f132d3fe7dbead63aeabee2d8e50ff
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2831689977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ded5843fc58f3ddd08b2ce57be07041699dcfaecf367c2b5b964475cb147ff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Jul 2022 19:17:39 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 19:17:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.0-rc3-win64.exe
# Mon, 18 Jul 2022 19:17:41 GMT
ENV JULIA_SHA256=fd861d6c4a97f5319cbb5a4b508fc16fc3aaacbe113fa5cbe31b37fa00e4f18e
# Mon, 18 Jul 2022 19:20:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 18 Jul 2022 19:20:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b4e97a338ebae8595c5fbbd57d88a74fe7beb584b9891bef16e7d9c3f4dcfd`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675d547bb1946edda8fab0d35eaa9541bbcbd6e002aee1eb62025d7bf7e7eca`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292ed2e65b39804dc581777c92aa01bfb8c3e6fb255a0880d4ac79e444121218`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87edb9d9009ed02be7d5d8c813db0daa41c6bd3098653d4d8b3a1fb0f997aeb`  
		Last Modified: Mon, 18 Jul 2022 19:23:10 GMT  
		Size: 159.6 MB (159639126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c0b87b16b9b6d5dd243f03ac900202d7c8d5568074be1509a1574065d29df5`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
