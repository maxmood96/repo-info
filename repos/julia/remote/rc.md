## `julia:rc`

```console
$ docker pull julia@sha256:8de265e806358719b11c54384212841f57536e24379ba1dc531e472cc6b865f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:76be42ab93b6d8eccbb34545254d13b9f815817c403a847cc8d48d349d7917de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345438249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cb93d6ec9b2d01baddd68336294b7c6c6ff9ed565ef88444c21de3fd114964`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:21:28 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Wed, 24 Jun 2026 01:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3975afc58614eff39a0ff598136d4746823623ea0bcb369b24787bddea2e9d`  
		Last Modified: Wed, 24 Jun 2026 01:22:15 GMT  
		Size: 6.2 MB (6248419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affdd98f5e9b429a02fa700ddf241b47a21c402063e3959920106c9a48463207`  
		Last Modified: Wed, 24 Jun 2026 01:22:22 GMT  
		Size: 309.4 MB (309404038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0274c4000ba766cfccb31668dc3b1743e3cae3295dd5d0c1e924b5223d31f440`  
		Last Modified: Wed, 24 Jun 2026 01:22:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:be142485c90d95e1eddfe8b37d5cd9131852b95b12a53a80cbc5d1c5303fb5dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a95ef595f84f41c09bb461ed9d899fc1b4ba00f060a06ef81703eb3c4f7e45`

```dockerfile
```

-	Layers:
	-	`sha256:aba389384b747595ba23f1325fe032748710f2eca4590cdcebcbd8bf39ef8853`  
		Last Modified: Wed, 24 Jun 2026 01:22:14 GMT  
		Size: 2.2 MB (2241075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:511f0136f5efa9d775bd948ec04e8c27e76813f637d6071c5fe57e6db690683b`  
		Last Modified: Wed, 24 Jun 2026 01:22:14 GMT  
		Size: 17.2 KB (17160 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:6e9531c40e69145866a3ad53b164ed1c059292b5a1259bce6a4291b029974da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370113055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b117acd443bedacf4d655b096bd0c376950e2fe81e81350e142a37cbae99e7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:22:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:22:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:22:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:22:01 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Wed, 24 Jun 2026 01:22:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:22:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:22:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:22:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43962426b0a67f987570cc5ac9f88405294106a4865e023f11afc3673cceef2`  
		Last Modified: Wed, 24 Jun 2026 01:21:18 GMT  
		Size: 6.2 MB (6155443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a40aae3cca8208fdc1ed86095790367a691303ab85515474dbcb8d315e676c`  
		Last Modified: Wed, 24 Jun 2026 01:22:54 GMT  
		Size: 333.8 MB (333808691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead70ef0251c2e3438bdb2fcbaa9ddb6f848abeb2ea7c76cfae4cf9144445cb7`  
		Last Modified: Wed, 24 Jun 2026 01:22:47 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:bd42d2af2aeebc17053d9c327c12f79c4c940b4a17d1fdd00045ad867e18595d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11955905b68085774ce17b8afd98345f83c33171a83a59cae60083915f32c08e`

```dockerfile
```

-	Layers:
	-	`sha256:b87c9655589bdf9505146007d1889347525179746630b0025ecd8ad3e078e455`  
		Last Modified: Wed, 24 Jun 2026 01:22:48 GMT  
		Size: 2.2 MB (2241375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe5f72d79e691c0484dedb2b67915a261e1f4528fe1c0ec7389059d57350d29`  
		Last Modified: Wed, 24 Jun 2026 01:22:48 GMT  
		Size: 17.3 KB (17304 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:5e8dc5f2e2888b549199005e02b18598c15eb56e8799e7ecf879ea91da32354a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281066630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f15cffc72c537deddb984650975acc7b2dd3be1b0abab0cb89255e8d8aaacca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:17:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Wed, 24 Jun 2026 01:17:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:17:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Wed, 24 Jun 2026 01:17:58 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Wed, 24 Jun 2026 01:17:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-rc1-linux-x86_64.tar.gz'; 			sha256='94c501d83aa46fad188894a31db093c6d065bbab94346645c775876066ec1b78'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-rc1-linux-i686.tar.gz'; 			sha256='1e758cfe0ba45a9b5313ff732ff5aa0d4f1927129e1b207e5e6c51e35ed9abb4'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-rc1-linux-aarch64.tar.gz'; 			sha256='0e08d6410e76a51b6825aed34c9e20fd5778b35cc4b406dd8eb8bd402d8df705'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Wed, 24 Jun 2026 01:17:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:17:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 01:17:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e0984cc9befec40a26034cc611913e433f8d6935a45a6334fbafdca50cee0b`  
		Last Modified: Wed, 24 Jun 2026 01:18:30 GMT  
		Size: 6.4 MB (6435919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2ab93c5ad21d689ca3efb429da0180202038919b3fe2fa51a85759c69b8102`  
		Last Modified: Wed, 24 Jun 2026 01:18:37 GMT  
		Size: 243.3 MB (243329129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57800ff0b8aeeaab60e91516d686dab4a38d2a2c36644e3af428eda8a5ea0c`  
		Last Modified: Wed, 24 Jun 2026 01:18:29 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:8fc9e488617f766fee27643d4d20947470f91edef2aff45a99ba6c15440f18c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02bbd31caab4cbe7745fb084a3ee21abbe1f6af5688817f644b84c7d3d08e8f`

```dockerfile
```

-	Layers:
	-	`sha256:1d61ef8a9a7b4f875d3031f31593dca8a1d8adca4f71920fcf49c8bdb9225bb0`  
		Last Modified: Wed, 24 Jun 2026 01:18:29 GMT  
		Size: 2.2 MB (2238210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a54ae5c103eed684fa0be9a5cb9ba01bf68d5a9105b62e3b218cd1e87de2bb`  
		Last Modified: Wed, 24 Jun 2026 01:18:29 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.32995; amd64

```console
$ docker pull julia@sha256:44cf21fd7bdc1d8fa3d9d9f9fe99681e1e2615a1824ffd1e2720f533ddda7620
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2591373237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a9255fe6b72bed57239cdc425b35d9d0da34bccc30ae1a7d2c653ad8db9c43`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:13:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:13:32 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Tue, 09 Jun 2026 22:13:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Tue, 09 Jun 2026 22:13:35 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Tue, 09 Jun 2026 22:15:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:15:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde3f87c92fa7d0ae280c09db445ee43c8fe0d6469fc2c7ef39eccb597a279d6`  
		Last Modified: Tue, 09 Jun 2026 22:15:30 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c87a936f114b0c6996d10ffc570b94029d36e6d6a298539678106eec789a259`  
		Last Modified: Tue, 09 Jun 2026 22:15:28 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9466b13032a821219324e7de900402ffb33a00e4177db57182f839e7fca360d0`  
		Last Modified: Tue, 09 Jun 2026 22:15:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f9377e14d74ada2944d6c5320eb71c56b4c77a3f26d8ba49b5b3aaeaa52427`  
		Last Modified: Tue, 09 Jun 2026 22:15:28 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cab0e0c1b628474f4eb962d3eb4f75d3961b788342e3f1da181ba4b2b33ce9`  
		Last Modified: Tue, 09 Jun 2026 22:16:14 GMT  
		Size: 312.2 MB (312223742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4810c7a706d6d8ad9f27312abfabe3640641c84ff3a0532af0025bfcc39cf9`  
		Last Modified: Tue, 09 Jun 2026 22:15:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.5256; amd64

```console
$ docker pull julia@sha256:6c63c9dfe569758a2979444ac62eea0aa03709e523cc9a73fe2cb29fc58e8fc9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2444460582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efe9a9d92b907444fd1836416e435af59bb4289e275216bc21e04bc9e0b1aa85`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:09:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:09:19 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Tue, 09 Jun 2026 22:09:21 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Tue, 09 Jun 2026 22:09:22 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Tue, 09 Jun 2026 22:12:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:12:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97b5912f4efef19e5de09c2f3306e758f70caacff609559c58cb4937c72d664`  
		Last Modified: Tue, 09 Jun 2026 22:12:46 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e264c8624fd27fab88a0273ac014d0e678d0c275d2680a9b2e4a1be6844d85b4`  
		Last Modified: Tue, 09 Jun 2026 22:12:44 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7c7a942d2c9b88f2be6f29d5f9a1d72facd244173e3f45d84ad1285ea4f6dc`  
		Last Modified: Tue, 09 Jun 2026 22:12:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d760474f3803b731b2cac7407de8a54299d72c14af17610e303d075ef7f8886e`  
		Last Modified: Tue, 09 Jun 2026 22:12:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42cf3ca7dccaa7cdec8d289632be3ca965d4e0b36ac65730164c0a912ac358d`  
		Last Modified: Tue, 09 Jun 2026 22:13:27 GMT  
		Size: 312.3 MB (312328542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50f64ceb5ffdf55481fcbe9075817a57ebeba60c2128e1fbed9284dabca67a9`  
		Last Modified: Tue, 09 Jun 2026 22:12:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
