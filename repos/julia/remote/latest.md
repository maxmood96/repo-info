## `julia:latest`

```console
$ docker pull julia@sha256:79c05957bf941e1b2844ba8c9faef7853736456eeeee00725167771095fbc27e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:2daa9a244cd8866c316c89798ba4656918d52b27685f59eecfcd3910e41072db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327478299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac96aa371957d166d1059a64f9dd8dbc4a3c3452cb09427cdb07deda438103b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:03:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:03:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 24 Feb 2026 19:03:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:03:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 24 Feb 2026 19:03:22 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 24 Feb 2026 19:03:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 24 Feb 2026 19:03:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:03:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de13c2dd0fd2f11f98d636aa2bbfe47e0f8e32c38019706ce61f95a8ca270dc`  
		Last Modified: Tue, 24 Feb 2026 19:04:05 GMT  
		Size: 6.2 MB (6246156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f5661ecc6c63790bb3cea114d514b8569ab25cfd3f4e0e6227a75fef09d1b1`  
		Last Modified: Tue, 24 Feb 2026 19:04:10 GMT  
		Size: 291.5 MB (291453143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba00fcfaacb25fa3519929aac256045f35dc509d1b7ee3bc9926e8415b75bc6b`  
		Last Modified: Tue, 24 Feb 2026 19:04:05 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:8420138534ba4d5d78b84f0e5b3021458f1f657579900fe067a36a88c9d41d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b4c76ea0dc9fd818f9edbb1c727cbd9fcc9eb41a64057eb1cc97c156476528`

```dockerfile
```

-	Layers:
	-	`sha256:d32c796d7fece069a13f1cb62d17b70aa277f129e2a0f7e3ba159a09eaebe096`  
		Last Modified: Tue, 24 Feb 2026 19:04:04 GMT  
		Size: 2.2 MB (2240221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9275b52d8865ccfbcc94ead8a57d41c2370201f00fd98009cb0f42cc6b2ea0c`  
		Last Modified: Tue, 24 Feb 2026 19:04:04 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:38f189b5d2a41133a0164cbdb60b43774a7c8e5437e943acb5955c069ca69d74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347548004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e184ef4dc752f91980794679bdec67f5d5903f35354cd434b33f34b62f5fbe9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:06:29 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 24 Feb 2026 19:06:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:06:29 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 24 Feb 2026 19:06:29 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 24 Feb 2026 19:06:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 24 Feb 2026 19:06:29 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:06:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:06:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db03341af746b495dbb4009956ec7b60ec54ae57e58272404f06f5355346c85`  
		Last Modified: Tue, 24 Feb 2026 19:07:16 GMT  
		Size: 6.2 MB (6154027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2502e68253830ce38d18ef433bbfea9ef460eec9b3f26b781ddffbd4900c1`  
		Last Modified: Tue, 24 Feb 2026 19:07:24 GMT  
		Size: 311.3 MB (311253511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3128338b6b6771687b563ba136b06982fb13ce20f0b2aef00256f0afae5a91d`  
		Last Modified: Tue, 24 Feb 2026 19:07:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:dcefcd28acc167f242a3ab10b9b75e58b1c265a77957bdeb5d602d138cddc4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a841c81b1cea1b63c8da64bd96b54db33e4fd9c1cc26b20ff7cf2281e76411c8`

```dockerfile
```

-	Layers:
	-	`sha256:99a48672c7a7dc05110390d357957b4e895e8835b902fee0c937461802c186f8`  
		Last Modified: Tue, 24 Feb 2026 19:07:15 GMT  
		Size: 2.2 MB (2240553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8c023752cce776d18303b2e230b3ca7970535d281be7473b68cd61d3c6e798`  
		Last Modified: Tue, 24 Feb 2026 19:07:15 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:fbee20878d20af4ee5374e712035ccdfdfd9b2cff765ae0c3648ce82170e9c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268936022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa194f686bc21d268680bda6a69b724c54289088b38ec596f851018a97bef1b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:58:54 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 24 Feb 2026 18:58:54 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 18:58:54 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 24 Feb 2026 18:58:54 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 24 Feb 2026 18:58:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.5-linux-x86_64.tar.gz'; 			sha256='41b84d727e4e96fbf3ed9e92fa195d773d247b9097f73fad688f8b699758bae7'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.5-linux-i686.tar.gz'; 			sha256='aa664f0e5936c7ee2ac093675ea532d33dee60fbb330e62ce45a1a4c4800204a'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.5-linux-aarch64.tar.gz'; 			sha256='2e5de844ea4462bfb08a5ba9fa5ae03532183cc0d9e724590e2c8df654f3e8e2'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 24 Feb 2026 18:58:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:54 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550378b12b3c18b6e1fd832cf7f9613bf9b0a84605431c653779f38364a1200`  
		Last Modified: Tue, 24 Feb 2026 18:59:26 GMT  
		Size: 6.4 MB (6433611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e848c4a445a3b078f2f2950d4eaffb8db3e078112a95ea232c198a55961f6589`  
		Last Modified: Tue, 24 Feb 2026 18:59:30 GMT  
		Size: 231.2 MB (231208122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8657d8d9865bfa3cc97cc23dd1563855b92fa0da6051deaae32392e5deb2834`  
		Last Modified: Tue, 24 Feb 2026 18:59:26 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:e718f5b2b1f9ebe1ff0302945273c6db40715f3c6a0a29a08304cd2e7c496600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf6bdaa15698c9fee1dee48219c17939f94f3d51ae85ee6d742babd6845733c`

```dockerfile
```

-	Layers:
	-	`sha256:06dc266445629fff0a0e242f964ace44f6604bc878c46ccef49c61f7d501cc59`  
		Last Modified: Tue, 24 Feb 2026 18:59:26 GMT  
		Size: 2.2 MB (2237346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9c6c3462c438fa6ed528c63b5fdf71d400d01f13a90bf9d0fe201c94e7a9b28`  
		Last Modified: Tue, 24 Feb 2026 18:59:26 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.32370; amd64

```console
$ docker pull julia@sha256:26fed03bf77315768437da7da712a2f328c8b1b8cac8051c598773a246a7c5ae
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251070899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5459db51f755279bcda92a316020302155ef6308bcc9b9097f803dc6200d5efe`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Wed, 11 Feb 2026 01:13:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 01:13:42 GMT
ENV JULIA_VERSION=1.12.5
# Wed, 11 Feb 2026 01:13:42 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Wed, 11 Feb 2026 01:13:43 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Wed, 11 Feb 2026 01:14:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Feb 2026 01:14:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ebd08ecafce1c314a35f93321236af74ba2d89445873606cbf6cde8bd3a26c`  
		Last Modified: Wed, 11 Feb 2026 01:15:09 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1a0fcb121f9dab830587148600c6c4deb87fe294485c75bf250458e3737dc1`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac78364a3a60882997b569d917c39824c76786078c56c98f217a383313edc08`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ef5db1d7661d7aaf4e9b0df0a716bc21ab2229d1a373a3418c6bee0947ca0b`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df0205b12d9ac3914654323c88534f6960ced5ac66adc8f6c5555fbd0faec99`  
		Last Modified: Wed, 11 Feb 2026 01:15:51 GMT  
		Size: 286.3 MB (286304404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82407043b8355a557b4f4f6e426d4cc8b9ac13a7346dd2f989142e3529dae81`  
		Last Modified: Wed, 11 Feb 2026 01:15:07 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4773; amd64

```console
$ docker pull julia@sha256:f2e460fe268c466fc4e21fae889fcdb344e346320f87fea61ce9df9c9d3b5395
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2149053289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdf76a844b45471e1d3ded5c52e66f6f2c0d28fd4fce94e383ad39c773df3c8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 01:10:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 01:10:16 GMT
ENV JULIA_VERSION=1.12.5
# Wed, 11 Feb 2026 01:10:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Wed, 11 Feb 2026 01:10:18 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Wed, 11 Feb 2026 01:12:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Feb 2026 01:12:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71099ac0ee59fcbe5d2e13acf798c85403706838f4e92d96421ae09af5314edb`  
		Last Modified: Wed, 11 Feb 2026 01:13:01 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb2fc2e8cbf0388dcd0ab151b24f61762379f76dfad3e5d9b7bb41d8eef1339`  
		Last Modified: Wed, 11 Feb 2026 01:13:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c57a54db8e955178464d8bc54373a734f9641c2d3040d8767aefa529b9f07`  
		Last Modified: Wed, 11 Feb 2026 01:12:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cc26f587094b6ac3dadd7234041b439a7892962cde9ddae2f9ec92fae838bd`  
		Last Modified: Wed, 11 Feb 2026 01:12:59 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c7c42ef1d5669ff8cf667c14eb8c829b6fe594b544967ca2c6fcc241ca379c`  
		Last Modified: Wed, 11 Feb 2026 01:13:44 GMT  
		Size: 286.4 MB (286389499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b56ebed73d303b518cb2bc53b143feb54fc045bc41950f109ce27f987eae89d`  
		Last Modified: Wed, 11 Feb 2026 01:13:00 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
