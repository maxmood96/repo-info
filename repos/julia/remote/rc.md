## `julia:rc`

```console
$ docker pull julia@sha256:1450537715b5800a2089dfcd06ba56ec0bf6aeba0fb793d8eff9d9873f129ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:a97d6cb1cfa99ab427357605f74f06ff533a5bdfebaf94aa1997b310e6016fdd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178353804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764424a8e482d00c6b8aa72205075a821a07116b1759ed3058fe455e3a5b424d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:54 GMT
ADD file:1f1efd56601ebc26a041a7b994a380ef68112b91a078e225753bee7b3196d22c in / 
# Tue, 06 Dec 2022 01:20:54 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 08:37:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 08:37:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 06 Dec 2022 08:37:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 08:37:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 06 Dec 2022 08:37:57 GMT
ENV JULIA_VERSION=1.9.0-alpha1
# Tue, 06 Dec 2022 08:38:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c657ed4e792f300d45d1ea5ffb71d052cae4e0d653142b277a3cba4d2cecfd7d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-alpha1-linux-aarch64.tar.gz'; 			sha256='595451736674c8f2e1cd8be514901cf47043ffc611078c1edcca7d7901ffafb8'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-alpha1-linux-i686.tar.gz'; 			sha256='c8b9312e9b210974a26e9abe3a6d70be9e30f1603a227a11bb2ce1c62351df07'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 06 Dec 2022 08:38:16 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 06 Dec 2022 08:38:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 08:38:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:025c56f98b679f70b7a54241917e56da7b59ab9d2defecc6ebdb0bf2750484bb`  
		Last Modified: Tue, 06 Dec 2022 01:25:12 GMT  
		Size: 31.4 MB (31412852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531e0415ed96aab85f2c297b695500e0d6f02118f2c6ed342ac2448e5bac00f7`  
		Last Modified: Tue, 06 Dec 2022 08:41:12 GMT  
		Size: 2.4 MB (2427488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ea97a0bf0cdab183dd69a26e2c158f5db4e667d9927106b34f224638681c0`  
		Last Modified: Tue, 06 Dec 2022 08:41:34 GMT  
		Size: 144.5 MB (144513091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81ce2fe7cb27ed559d11f7639575a76f33c09fcb461bb56a79b57fa4f05ea6d`  
		Last Modified: Tue, 06 Dec 2022 08:41:11 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:12de2323bc641536255c8830aca231954d39e43044b0562b1ab4245aaa45bd6a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.8 MB (170804791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea07387fbdce3276a226af7d138852a217fde7518ba83f27eebed14b4b91660`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 03:51:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 03:51:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 06 Dec 2022 03:51:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 03:51:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 06 Dec 2022 03:51:41 GMT
ENV JULIA_VERSION=1.9.0-alpha1
# Tue, 06 Dec 2022 03:51:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c657ed4e792f300d45d1ea5ffb71d052cae4e0d653142b277a3cba4d2cecfd7d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-alpha1-linux-aarch64.tar.gz'; 			sha256='595451736674c8f2e1cd8be514901cf47043ffc611078c1edcca7d7901ffafb8'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-alpha1-linux-i686.tar.gz'; 			sha256='c8b9312e9b210974a26e9abe3a6d70be9e30f1603a227a11bb2ce1c62351df07'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 06 Dec 2022 03:51:59 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 06 Dec 2022 03:51:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 03:51:59 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98701f6087c1d3a7659e32a6d44c77192664fd6fa07cbb399977e76cb6fbf76a`  
		Last Modified: Tue, 06 Dec 2022 03:54:15 GMT  
		Size: 2.4 MB (2415867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660d0c458892f03fc65bf5797340bdcc223adccad28a62359d7ebf7f334dd63c`  
		Last Modified: Tue, 06 Dec 2022 03:54:32 GMT  
		Size: 138.3 MB (138328229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea522580f6dd00d3bb141d9cbc787ff3a936910c2730c07ad545f81603df9a2`  
		Last Modified: Tue, 06 Dec 2022 03:54:15 GMT  
		Size: 375.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:b53849dc536285e5c635637c52cba32dc40ede4918b5c6555b1d8140bb7b0cb9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176448538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a008f9ca679ad9a247b754711f7538a9da0d0f9335adf599641e9deafc381cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Tue, 06 Dec 2022 01:39:52 GMT
ADD file:3912079114d3e8e334fdf795a4793a492f37989804e1148b98fafbd4eaa00b7e in / 
# Tue, 06 Dec 2022 01:39:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 14:09:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 14:09:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 06 Dec 2022 14:09:29 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Dec 2022 14:09:30 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 06 Dec 2022 14:09:31 GMT
ENV JULIA_VERSION=1.9.0-alpha1
# Tue, 06 Dec 2022 14:09:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.0-alpha1-linux-x86_64.tar.gz'; 			sha256='c657ed4e792f300d45d1ea5ffb71d052cae4e0d653142b277a3cba4d2cecfd7d'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.9/julia-1.9.0-alpha1-linux-aarch64.tar.gz'; 			sha256='595451736674c8f2e1cd8be514901cf47043ffc611078c1edcca7d7901ffafb8'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.9/julia-1.9.0-alpha1-linux-i686.tar.gz'; 			sha256='c8b9312e9b210974a26e9abe3a6d70be9e30f1603a227a11bb2ce1c62351df07'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	command -v gpgconf > /dev/null && gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version
# Tue, 06 Dec 2022 14:10:00 GMT
COPY file:92a2f9b3b9de38e57462f85dbe804b0eae9fea8a95aa9bfe9d3c2b95000ae42c in /usr/local/bin/ 
# Tue, 06 Dec 2022 14:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Dec 2022 14:10:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:01cb95e209fce595702ddb2b5ed266e2a01b6687efe67d201d74a5aee9595995`  
		Last Modified: Tue, 06 Dec 2022 01:45:41 GMT  
		Size: 32.4 MB (32393046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ddbe3eb89024e6bd5a622ad666b8ad17da6a67d9fbc3de5b0e97f560c39ccd`  
		Last Modified: Tue, 06 Dec 2022 14:13:33 GMT  
		Size: 2.3 MB (2327570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d337ac8d0699f2786fcca6a862db68b18c6e3c175227e67d128086a1d1928cb`  
		Last Modified: Tue, 06 Dec 2022 14:13:52 GMT  
		Size: 141.7 MB (141727549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74705e7fce3dec39cbd72dc6336737fd0f2efe16da98c1fc49732717981929c3`  
		Last Modified: Tue, 06 Dec 2022 14:13:32 GMT  
		Size: 373.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.1249; amd64

```console
$ docker pull julia@sha256:3fb5a907eafeeff67d2e56b3e76380521f49a6e1e33665b752cc1276b1a5cfdf
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2636588006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae8c503d59b2e966221a7efb4bb58f3a3597012fdecd3ecc3ff4eacef3e8d09`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Tue, 08 Nov 2022 18:28:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Nov 2022 22:14:23 GMT
ENV JULIA_VERSION=1.9.0-alpha1
# Fri, 18 Nov 2022 22:14:24 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-alpha1-win64.exe
# Fri, 18 Nov 2022 22:14:26 GMT
ENV JULIA_SHA256=b9cf18544d67e015fc8679e10deac29bef56758f1a88021ed485b5719bca7eae
# Fri, 18 Nov 2022 22:16:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Nov 2022 22:16:15 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3becc14271944025e3fa6c2ef2689bdfbf09bfc54ec339115d3082df315898e4`  
		Last Modified: Tue, 08 Nov 2022 19:38:57 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d0bfe3b39cdda5f721c9ea441d6dc83fd2ff6631dac275b841bb069b3feb46`  
		Last Modified: Fri, 18 Nov 2022 22:25:50 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405317f7b8a3e05e9763ba45b21c35262598c2495b446c7818532cb6c602bc87`  
		Last Modified: Fri, 18 Nov 2022 22:25:50 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e09d9e2e3db36377f72a07ce34af9fcb90dc3f4645856fa877fcda879daaf0`  
		Last Modified: Fri, 18 Nov 2022 22:25:50 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de006715b00b5ae9716ce4a3e3ec4aacee009f3c81e317679f4de75b3364993`  
		Last Modified: Fri, 18 Nov 2022 22:26:29 GMT  
		Size: 154.8 MB (154812245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773933f8a814ece8ccf94f04679dee85c425d0e161da53ab6f5b402592194eb3`  
		Last Modified: Fri, 18 Nov 2022 22:25:51 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.3650; amd64

```console
$ docker pull julia@sha256:cd2dede4419d4bacfff6295110c7bf2cb4b8bae446240f1e65d6f8d3c99d8625
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2933178352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcef2bf5cf948360766779b835c4d744c393ad42132f666f9d1e68c3a255a2f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Nov 2022 22:16:24 GMT
ENV JULIA_VERSION=1.9.0-alpha1
# Fri, 18 Nov 2022 22:16:25 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-alpha1-win64.exe
# Fri, 18 Nov 2022 22:16:26 GMT
ENV JULIA_SHA256=b9cf18544d67e015fc8679e10deac29bef56758f1a88021ed485b5719bca7eae
# Fri, 18 Nov 2022 22:19:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Nov 2022 22:19:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf77cdf7c0f68b4c3af4ab67c27f66782238f598419bf4c719a181294f92a5a6`  
		Last Modified: Fri, 18 Nov 2022 22:26:42 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136ea8bb969a82d49c5de30944fe3a83037bbee963a68923e23d152739f42710`  
		Last Modified: Fri, 18 Nov 2022 22:26:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4251b32cc13417651b00910d2eb5c317c060cf6be6000cba881ef6275c74765`  
		Last Modified: Fri, 18 Nov 2022 22:26:42 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a092561bf76d4f4a07eadf81a04b7c39dec3c7465766c628277d2cc0ceefa41`  
		Last Modified: Fri, 18 Nov 2022 22:27:19 GMT  
		Size: 154.6 MB (154584411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bee2e39a34d91f650cf6a753b89364474f38061a115de139b7b86bba7883c1`  
		Last Modified: Fri, 18 Nov 2022 22:26:42 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
