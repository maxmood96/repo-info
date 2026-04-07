## `julia:rc`

```console
$ docker pull julia@sha256:79098518427ebd10dd35fde3f1475c0cf6d297e85b25f60c145331d0d1c6a29f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:f2fb4614d8b6c29d8f2f754e075f8299d25b34319aff503663b6b3370215eb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344823135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176456319c77ccb728c8539f91931f1dff2eaa1100f0d7ab145d476e4d90a74c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:23:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:24:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:24:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:24:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:24:01 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 07 Apr 2026 01:24:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta3-linux-x86_64.tar.gz'; 			sha256='02111690b460ad1641d10fc920f3000a6254916d2f53b6d0f5f7482f47283e62'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta3-linux-i686.tar.gz'; 			sha256='3f0f1a362e611559b58acb71a50a130b9fc53273d157755cb7ac8f0fa7d99ef2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta3-linux-aarch64.tar.gz'; 			sha256='56043f2572c169a4d515b201f192d91792b4f5dfc8f1d90f595101a240693348'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:24:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:24:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:24:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd06d5409b6c08d7ef092bfa5579c710dbbfcc632480f9c312ba81ce3866b9e5`  
		Last Modified: Tue, 07 Apr 2026 01:24:47 GMT  
		Size: 6.2 MB (6247115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c27b62df8456e37791407f78ac9862bda42070a257cf2486167fcdc150da1c6`  
		Last Modified: Tue, 07 Apr 2026 01:24:52 GMT  
		Size: 308.8 MB (308800010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894a106d16d3e5dcef7f3f00155c25bf6923f5fac4652eb04b38f31e1927185b`  
		Last Modified: Tue, 07 Apr 2026 01:24:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:072d5a4aec5a7390abc28801624f91ecf7eb5d0852e5e741a0283f30925e15b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879424f6c420c8a96f4c63cdfb79150676ef6f233788c6f293c840c0a0966d57`

```dockerfile
```

-	Layers:
	-	`sha256:065a8ca80aa73f83a43b841df7f1488e57a9f297e7e2cf630d4ec9d5f26b3d15`  
		Last Modified: Tue, 07 Apr 2026 01:24:46 GMT  
		Size: 2.2 MB (2240915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:906fe8aaf1fc13eb0e0d9fa69433d310f23c31c70222e0e54fb6685c089f4569`  
		Last Modified: Tue, 07 Apr 2026 01:24:46 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:8ae205128af7cb3f3912c5b7774be2e11da6cfd41a98a28add0c43bd76ecc3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369135194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c0704c13dab1222dc24db1138768fe45a1739129cac4e687b18b707ddf80d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:21:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:23:09 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:23:09 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:23:09 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:23:09 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 07 Apr 2026 01:23:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta3-linux-x86_64.tar.gz'; 			sha256='02111690b460ad1641d10fc920f3000a6254916d2f53b6d0f5f7482f47283e62'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta3-linux-i686.tar.gz'; 			sha256='3f0f1a362e611559b58acb71a50a130b9fc53273d157755cb7ac8f0fa7d99ef2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta3-linux-aarch64.tar.gz'; 			sha256='56043f2572c169a4d515b201f192d91792b4f5dfc8f1d90f595101a240693348'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:23:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:23:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:23:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1942f1b89988dad64aafe3423da5e52c0a6ad524ed7dad152a0c88682915d33`  
		Last Modified: Tue, 07 Apr 2026 01:22:23 GMT  
		Size: 6.2 MB (6154476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a569852368257a668f2ff11227f6273039a7aa2a981f8e2718846fb6b68643fc`  
		Last Modified: Tue, 07 Apr 2026 01:24:04 GMT  
		Size: 332.8 MB (332841798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e08f6a5bdd4dae0c118e497d4aac08ecb8032b5d60ed7c4aae971fbfb61712`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:8afd0bf15c3a04582627e7748da1d849cf8a73ccb9edc86ebae88f7fc7cae4db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dee8ab74e87769cd6ca862fa1627c3bc17971a5c9877f55a2121ed6367ebb63d`

```dockerfile
```

-	Layers:
	-	`sha256:70a7c8e7cf32a85cdea67ad3e343724b2a940afebda73d197e19c2cc666d7631`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 2.2 MB (2241223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c34c61fe80de16c19798eab8ed2858820576bf4a19b58c5c160eb88ad2cf819a`  
		Last Modified: Tue, 07 Apr 2026 01:23:55 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:3c62b36d004a99c7e55b639a3311c34bb14ee5219e0267e99e483bba43e0c802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280483391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af26f8f5520cdc92204769753d96062c3776b1bc9db46ccd985030f07b68b467`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:19:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 07 Apr 2026 01:19:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 07 Apr 2026 01:19:14 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 07 Apr 2026 01:19:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta3-linux-x86_64.tar.gz'; 			sha256='02111690b460ad1641d10fc920f3000a6254916d2f53b6d0f5f7482f47283e62'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta3-linux-i686.tar.gz'; 			sha256='3f0f1a362e611559b58acb71a50a130b9fc53273d157755cb7ac8f0fa7d99ef2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta3-linux-aarch64.tar.gz'; 			sha256='56043f2572c169a4d515b201f192d91792b4f5dfc8f1d90f595101a240693348'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 07 Apr 2026 01:19:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 01:19:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 01:19:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce1f27a2975669231338ea7392707bfad311e6772e7ad198939bbe2209bcfd3`  
		Last Modified: Tue, 07 Apr 2026 01:18:42 GMT  
		Size: 6.4 MB (6433792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5e320163ef808366a8b7511b9030f22536589f46b9fbad72e75369bc961d44`  
		Last Modified: Tue, 07 Apr 2026 01:19:52 GMT  
		Size: 242.8 MB (242757975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce2477ff6ba8b3bea5b4e91440b7b9804974ca2077417c75f576462514fe41e`  
		Last Modified: Tue, 07 Apr 2026 01:19:47 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:1fe81a28a7890378e485e9c5d5bfca2374225c3baab8a0da6a603cf4adf389b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad197af5be93c532220f91fd1b66fd04cbcb40e6e91f24b8ab5d4988d199700a`

```dockerfile
```

-	Layers:
	-	`sha256:c5dd57cc7577398e98b89f2bc7d6d11fcec430490ff8d39970b5ac563c13bc40`  
		Last Modified: Tue, 07 Apr 2026 01:19:47 GMT  
		Size: 2.2 MB (2238050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a1bd88888b71159ffb4e54d75b0c855d7650cce79c5e2f057ce9d3c3716d347`  
		Last Modified: Tue, 07 Apr 2026 01:19:47 GMT  
		Size: 17.1 KB (17145 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.32522; amd64

```console
$ docker pull julia@sha256:82723a5251b34305774e6bcfb591ac8e2aeb82e95dd0b5139789f66f6f4cee54
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2392496983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f0c88888e4f40c3ea823785ab2c75c562bb005554b65593be134f3ce5f721`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 17 Mar 2026 17:43:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Mar 2026 17:43:08 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:43:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta3-win64.exe
# Tue, 17 Mar 2026 17:43:11 GMT
ENV JULIA_SHA256=3ac4b3824830783ec9661cdbcca93875faea1c2ffb33568aeba1924e26466cb2
# Tue, 17 Mar 2026 17:45:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 17 Mar 2026 17:45:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d1c2ce2f27ffb6077908fa6292ca7dc54b4a8e61f8005acb358da8ef863d2a`  
		Last Modified: Tue, 17 Mar 2026 17:45:49 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050118bc471de0e012aaa76dffe4fdb2109c671409e9d52fad345db6ed30d5d`  
		Last Modified: Tue, 17 Mar 2026 17:45:48 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9f0c2b4bd40b962bce4b88bffb05dae543f83761207a9096e05dff1de83e4b`  
		Last Modified: Tue, 17 Mar 2026 17:45:48 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed39dca27b5e7548d7507e2584844a2ccb870c96c3a502927627f99403bcda`  
		Last Modified: Tue, 17 Mar 2026 17:45:48 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19484f5a86b507e31ccec76f0ee807c2acd07ff490c8a42e9bb90932548df35e`  
		Last Modified: Tue, 17 Mar 2026 17:46:34 GMT  
		Size: 311.3 MB (311294398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965843dd101ee712b625f1b8d725c43ecb4a32866ae4680163fb7c83d291e3d3`  
		Last Modified: Tue, 17 Mar 2026 17:45:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.4893; amd64

```console
$ docker pull julia@sha256:51864206a6a750618a20db2a79162012afb1ae4f708b55aadb2ed88d8ad521df
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2293705592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c34cfeb418e0b08183960b531dbfee95860448a40fce85947f5b5a2194ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 17 Mar 2026 17:45:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Mar 2026 17:45:14 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:45:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta3-win64.exe
# Tue, 17 Mar 2026 17:45:17 GMT
ENV JULIA_SHA256=3ac4b3824830783ec9661cdbcca93875faea1c2ffb33568aeba1924e26466cb2
# Tue, 17 Mar 2026 17:47:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 17 Mar 2026 17:47:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26117b6ad3a47350d4334b6cd3202fc105adb14741b00113c3bf829d9dcd4019`  
		Last Modified: Tue, 17 Mar 2026 17:47:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813213f4b6ee08dbdffb17dcbe3313427f7d1e4faee61f9283129382b57d2423`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e24179a211b65135995fd9726b7e6f6245af633fc2f9b61af57bbc2408070c5`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec5be4f0725c7d9918a025c419253fe8343dfb1461e8cd8803b28b5b28e2a6`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8659cf43fcfa5cf93d4df4740eedd56f682900baf106116ee34d046d60bfb436`  
		Last Modified: Tue, 17 Mar 2026 17:48:37 GMT  
		Size: 311.4 MB (311417685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7887c8b203340d29d1cac05bc5f78ff15c95fe4727325d1dbfb2e331c06cee7`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
