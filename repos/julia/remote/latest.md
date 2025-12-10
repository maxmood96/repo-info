## `julia:latest`

```console
$ docker pull julia@sha256:e0976e892bebcbd29ea15b6660b5e0d9b20e03a6adb257f2ee505919d4495fe4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:2439560d508d999ab9359984994c41347831a0b3c5857d960ef4670348b0d5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.0 MB (326001539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dd7292e224db22bfc83fd90a2884afd1cd3401f978834f86cefbf8eaea6c60`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 08 Dec 2025 22:37:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:37:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 08 Dec 2025 22:37:32 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 08 Dec 2025 22:37:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:37:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e987787d89376a395d6f5283856c66ba5bf585a63dbe12c8abd8503a03c31fef`  
		Last Modified: Mon, 08 Dec 2025 22:38:33 GMT  
		Size: 6.2 MB (6242804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfef7656fab117dd116e632a4a6ddb25db99780115cdd963e1968920751c2f94`  
		Last Modified: Mon, 08 Dec 2025 22:38:57 GMT  
		Size: 290.0 MB (289981868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c8a474a2ebe4de0ffe9347791343708e7a9280edfab035d9d47ec5445b6445`  
		Last Modified: Mon, 08 Dec 2025 22:38:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:290a4f515c3e99551863f14fb7dd3c2f300be0668dd7d5b6a647ac67babbab36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95dc478accda3a3f4f547c58d1526ccb4be514ea563bcd9266c393d78c19772`

```dockerfile
```

-	Layers:
	-	`sha256:165d54f96e2c9912a1301d3a8acbce2c0b7a8b3a8c75eab1613be853e2e05c28`  
		Last Modified: Tue, 09 Dec 2025 00:03:02 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90212f55a35e3805431172cd8de1194ca2798abf97edf68bd988adc0313b4721`  
		Last Modified: Tue, 09 Dec 2025 00:03:03 GMT  
		Size: 17.7 KB (17688 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:a032030c89942ed7c1dd3bd7e70d894bc20bd81565c7a8f3016cc049b8d6c097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347276265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221e3610123ff05c9044a79fd42a56c7e6cba46096099da5ed3f2a35e4be987c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:35:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:36:25 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 08 Dec 2025 22:36:25 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:36:25 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 08 Dec 2025 22:36:25 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 08 Dec 2025 22:36:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 08 Dec 2025 22:36:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:36:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:36:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee263368a7e028dc6e4c1dfb5d1be63a24575826f7ce8300926b354a26781b`  
		Last Modified: Mon, 08 Dec 2025 22:37:27 GMT  
		Size: 6.2 MB (6153474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede9daf9f0bbecc0137d2a69d7efdb1ebf720c716e5e58bb3b374d0e18ce0a80`  
		Last Modified: Mon, 08 Dec 2025 22:39:02 GMT  
		Size: 311.0 MB (310983797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf0f10da1f7b1088a646c12e7681da6261da77ea474d69aada37c8305af9dcf`  
		Last Modified: Mon, 08 Dec 2025 22:37:28 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:ae8d1d8f849f93689dbad98308883fba9a7fc95720f26cecd12ea8464c2f12a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ad6dee9f2e6003bd30b0df98ebf19ca70553f1dcc1e3072b437ea9405e4643`

```dockerfile
```

-	Layers:
	-	`sha256:3ef07554e755711916a6527854309fb9bb3c55e09aeef2dc76fd18e6351d53a5`  
		Last Modified: Tue, 09 Dec 2025 00:03:08 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c138ba067173fcbdc47a99078bf0d0cf7add4315491fe1b23d294f3f1470879a`  
		Last Modified: Tue, 09 Dec 2025 00:03:08 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:0ba1750c14db502896120ad57cbf1aa098bdf1f432a9e86bf825417fb868c95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268889819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136f5c4263ee1249257b948eb7b7dce96f37db8ddfd9bcdaa75f1fb716ec675e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 22:35:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 08 Dec 2025 22:35:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:35:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 08 Dec 2025 22:35:32 GMT
ENV JULIA_VERSION=1.12.2
# Mon, 08 Dec 2025 22:35:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.2-linux-x86_64.tar.gz'; 			sha256='a6d0c39ea57303ebcffa7a8d453429b86eb271e150c7cb0f5958fe65909b493a'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.2-linux-i686.tar.gz'; 			sha256='e7492e2454ecfd03f4da6fd30fb60391d184128bf683c96d1ea6f13cd35a20c8'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.2-linux-aarch64.tar.gz'; 			sha256='0383a2ce378b64356269f6f15e612f344523f507a9753f71a0b64ca02092445b'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 08 Dec 2025 22:35:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 22:35:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:35:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c41a608a53984ecd78ece7091a6f0782d16bcefeedd081d9a39eec4d3853d28`  
		Last Modified: Mon, 08 Dec 2025 22:33:59 GMT  
		Size: 6.4 MB (6427663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01884f9b1cdd4ff47977ac4f765fffe06b3abcec2cb54e88afbec1ebab27cfd`  
		Last Modified: Mon, 08 Dec 2025 22:36:21 GMT  
		Size: 231.2 MB (231168719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b1960dbd9d150c7a244fa7a45c4259f4abb3ee44960d9f38e3c8a55af26452`  
		Last Modified: Mon, 08 Dec 2025 22:36:11 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:3004dc9bed2c5ebe73652ef48e4123787b17e6010bdfcac5746632f7c05a0aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979d4df36326bc4b0c788e1ee2bf9decb176d99080e7fa51b5d9cdf29dfbfe95`

```dockerfile
```

-	Layers:
	-	`sha256:cdda7e7bd38fb8a7c0df1fc45f58b6ee7fcfa2f1cd993537f654d3d4e166d20d`  
		Last Modified: Tue, 09 Dec 2025 00:03:12 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c55885e7e251c922f7e2febf761dff6c266b24f7611818308fd5ab26cddab`  
		Last Modified: Tue, 09 Dec 2025 00:03:13 GMT  
		Size: 17.6 KB (17635 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull julia@sha256:f646c262c693923078dd1367a8892bf9f82e257360efd5d10672d0201a780f02
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3639145989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda9a693e86e998532ec21e54d9a5602e6a069083f23ba1df78fb28fd01aaeca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:35:21 GMT
ENV JULIA_VERSION=1.12.2
# Tue, 09 Dec 2025 20:35:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Tue, 09 Dec 2025 20:35:22 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Tue, 09 Dec 2025 20:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:37:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c64c7dc565d03eb3e9f39894e67ad9fe74d54f61e84975b3f57b9f2972a79`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66fdedb62e9363240d1648636c3f97dc5c9695d52cb30e1bdff0f88d750d47e`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc37f0905d73ef1b5ac18675b08df9f750e89fa97ccf7f10ac44e6a412b2c64`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d45161174a9487b09781f63981fefc9959ff659c2f61f30c615180c879e225`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efed2071fb98ca5345ad7ccc3118e0972f266521b883de458c2b8c1d08d98b33`  
		Last Modified: Tue, 09 Dec 2025 20:45:21 GMT  
		Size: 386.0 MB (386019029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6395f80ded2d1defcb8360787857a8b0e66c0742878fa7c61faf7b12d849cf59`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull julia@sha256:5a6338c253e019e0204d9e2d9d98e89b801cb075a5dbb126b1510d83f15aaa56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2165978101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480c27f3a3c9cc5e0f01c408773a3f602c0350fea897997ae0aa8e54cb243895`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:32:46 GMT
ENV JULIA_VERSION=1.12.2
# Tue, 09 Dec 2025 20:32:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Tue, 09 Dec 2025 20:32:47 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Tue, 09 Dec 2025 20:35:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:35:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4337b0b452250939272a24a7d25392c5f6351fbf9da067a0d397cefbb4266c7a`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c6c5577de4e171f25b235ca6f8a0adebf834fe9f056f30433b8639145f99ba`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa80e94aa03accb23f8d444de9fe4c73941bbf916c68dcfe845cd2118f81856`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f0c9df9c3e0662ae962acfeec828cd6bb17996ee6a8444f2d4c25505b1ddaf`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2147e4adbcc9e9f51209be098aa739258b406e821fa9d85698a386109e14c1f1`  
		Last Modified: Tue, 09 Dec 2025 20:40:57 GMT  
		Size: 386.1 MB (386092289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21433acfd914605fe1899281b94af10aa9480656be49a66b9d81c4de427085f8`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
