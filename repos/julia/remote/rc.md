## `julia:rc`

```console
$ docker pull julia@sha256:90f015931f3d76cbe7ff8fe20bf6246e3393efd5e24c058300e4039ae0bd9044
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:5cf3764e300c70eb35b031346a48f66c3212a83fa5766a74e8927c2c21aefef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.6 MB (335642051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20845c46d5eca5656d4694f94353f867919223618d50ba58157d6466eeb93f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 04 Apr 2025 18:28:32 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c3184e8c3b5d47f4223fe62905ce33437868543b6a5cd6898c4aa907a9f2`  
		Last Modified: Tue, 08 Apr 2025 01:12:58 GMT  
		Size: 5.7 MB (5713471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b67c69e186229fc396b3b309b73f6ff92a1dba59f7eb20acdef2c7cd3358500`  
		Last Modified: Tue, 08 Apr 2025 01:13:04 GMT  
		Size: 301.7 MB (301700950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87af4a6aee6dfb167a634f92ef021c26d2320dadcef7b45191497363218c243e`  
		Last Modified: Tue, 08 Apr 2025 01:12:58 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:fd9cee21ed32cbb5d4844fb3865dafbd09be80f59a778ddacef133f48cfd4f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795f238f8fe73f16ca923432db01379d362e193c1179b3d629e00e9b789b81f7`

```dockerfile
```

-	Layers:
	-	`sha256:5e9369321948278f7e53c95d70e7c3f5628e66bbd95a7cb642e5ff663c27ac77`  
		Last Modified: Tue, 08 Apr 2025 01:12:58 GMT  
		Size: 2.4 MB (2446248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9f49bf70ed8f59b34e7f94e58f5472f75655893135729ca5513c32c9702802`  
		Last Modified: Tue, 08 Apr 2025 01:12:58 GMT  
		Size: 17.3 KB (17271 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:10076ec2effa56067a347aa9a5f0298b1f884403019c05c82a46a109cbc3147e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.0 MB (356968105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aba99f9c12a7609ccc170d3fe416d4d077e3697be774db01fca6148e5d2df3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 04 Apr 2025 18:28:32 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ebab4277db2f09d781f920b005edfb39dc7a867066124ff7bf7f1d1f1caed1`  
		Last Modified: Tue, 08 Apr 2025 02:05:17 GMT  
		Size: 5.5 MB (5538304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9345e7da90b6b2ddaaba8f68ee87598976f76a6bf410c5e830740ec5ee4edf3a`  
		Last Modified: Tue, 08 Apr 2025 02:05:24 GMT  
		Size: 323.4 MB (323363110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f7054b2082260932966b6578eddbb5ddc9df9d7d730b31fe11be705ae8e6f`  
		Last Modified: Tue, 08 Apr 2025 02:05:17 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:798cba1c90d3ada514902ca382132c3134ac839209963132be962103d8205b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7982ee456736a6aa2181c0837cf7ce074eee4bb116d20bf778447787d7443ec9`

```dockerfile
```

-	Layers:
	-	`sha256:9a78bf1fe0b5d1b8cefba95ad9ee731c2e7c9efefc5fd64ff5ae249e2c46a0ad`  
		Last Modified: Tue, 08 Apr 2025 02:05:17 GMT  
		Size: 2.4 MB (2446547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9337d471d8d71df4c1292798f0cfb053f938709b2817d1adbbec8878fc7d7a43`  
		Last Modified: Tue, 08 Apr 2025 02:05:16 GMT  
		Size: 17.4 KB (17413 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:fba6087efda29b7cc6882eac7006b5c959f8c86024a7af4658758870eef0e07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275647139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9501e241b4ac74531b1f7a7ed163fc3d5e038f6701fc9f217530f2fe36707db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Fri, 04 Apr 2025 18:28:32 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Fri, 04 Apr 2025 18:28:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Fri, 04 Apr 2025 18:28:32 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 18:28:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-beta1-linux-x86_64.tar.gz'; 			sha256='be66effc43fc8b870d09d74b25dfe365ca32733c7b735df28f4a7fadfcff23d1'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-beta1-linux-aarch64.tar.gz'; 			sha256='257b74706f1cd36d0c45beb921f9abb81129257fd6e957cc4cf779894e624a3f'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-beta1-linux-i686.tar.gz'; 			sha256='4e0ffe430529bfb127482d9965a1e711965435517739aed112898dee50ea1da4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Apr 2025 18:28:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Apr 2025 18:28:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cceb9282fa3c9188dbf34bf86716063a557120164e1d1f1ed37ec09c0808c31`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 5.9 MB (5872260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870b0c5acb49cf07a89a20b92993a3f2689202a6725c1bd5e4645c65a0443976`  
		Last Modified: Tue, 08 Apr 2025 01:12:54 GMT  
		Size: 240.6 MB (240563780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f0fa32966ffefdfa7bc655f545ea21d644e7eac53d92b6620fc870ddaa23f6`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:53510b1f0208d42e267fbf3bc4931d3059e34aab3b86a842ba4664a17a5fa568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2460558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20073494783fce610bd14bbd4d72f3d09586e768f8884e85be7ba711d462e1e1`

```dockerfile
```

-	Layers:
	-	`sha256:ed6d5cd241af549473f718a5e0cd8d6411403b7c18eb4c898e44f66082aa20de`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 2.4 MB (2443331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d906768834aa1bcac9899d7bf4431299fb2b750183628c23bfde86948cd3d3e`  
		Last Modified: Tue, 08 Apr 2025 01:12:49 GMT  
		Size: 17.2 KB (17227 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.3781; amd64

```console
$ docker pull julia@sha256:38a4688834b09230471668f625747043c8115544444886e9c8481701526a8388
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3689718330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b990ca274f7f09fbc591e36d3aaaf2a0570e13f65827b84eee4970276f46eb5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:13:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:13:39 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 18 Apr 2025 03:13:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 18 Apr 2025 03:13:41 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 18 Apr 2025 03:14:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:14:55 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d847cb8729cc156a33f45c8c7fd3dba8d388fe1250452da78b91c429cac4143`  
		Last Modified: Fri, 18 Apr 2025 03:14:59 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9293df24207b4274e8ed7b37864525eb87c3c117a30061355bd7ecd0208ea130`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6819b0563ab53578e347dbb7d0fedfa705d74b359dcfc728656bbc991e85a`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c4090a6becae243511e5f4ccbc3b40b8d8fce71d490360bc9a11d92ce9614c`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cda6730a3455bfd35603b180c1776210a5e2a9829133041ccb893f124c52692`  
		Last Modified: Fri, 18 Apr 2025 03:15:44 GMT  
		Size: 294.6 MB (294550449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df01aa3bad151b8392149d9e97bd5dec8dd71f6835fe3cee04564fdf2e6c93e8`  
		Last Modified: Fri, 18 Apr 2025 03:14:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.3566; amd64

```console
$ docker pull julia@sha256:61e62bac5695e0ab3a86ab2cd9244acbfe12bcb374b2fac5478e42dbeb18b706
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568050577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7315bd3eda65b33c5ba73df3a449b6ef70d7f6243312dbe162d3f6297d3d86fd`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:19:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:19:47 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 18 Apr 2025 03:19:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 18 Apr 2025 03:19:49 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 18 Apr 2025 03:21:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:21:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3568cbdbc43f2fb73f80e4cb09a4c8cb71d414c5c82ea37bbf228fa2d87f8`  
		Last Modified: Fri, 18 Apr 2025 03:21:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9494a98b0128ae2301ef8402b5dc2148714b22aa597c4345d06c2a1307d7d32a`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f94dbfdcc063cbe794e4b806184800c859fdd83f969a41229f55c06feea40d`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad27b45c50068f924f3a10356825ed81b314cdc2e661ae9641c867a9df94392f`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a67ec52f702b09267c549dc67f22904376deea6317b6859e8cca05499f805d`  
		Last Modified: Fri, 18 Apr 2025 03:21:51 GMT  
		Size: 294.5 MB (294461605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d909081ab78526e7e396945acf2d46386f93195387579982855168a452f8e9`  
		Last Modified: Fri, 18 Apr 2025 03:21:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.17763.7249; amd64

```console
$ docker pull julia@sha256:a9b0afd064ca2650750f9bde62acf4c60f291950c529e6c461277054cc172525
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459989078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90a7e3eac73cc314638b907db197ef43213cf8e86690c031540cfeb0072fda8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:14:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:55 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 18 Apr 2025 03:14:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 18 Apr 2025 03:14:56 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 18 Apr 2025 03:16:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:16:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea57d6e0a3fd854ce9629fe9fe87f545ffffa36f52dd5c56e985a47f44289670`  
		Last Modified: Fri, 18 Apr 2025 03:16:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b463d1e95170ef10a02abcd943e06f1b315fb61ddbdcccc3d0f4573fa2d788`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a35d996f03bfacd5085156de4e2220699d1a19d028f422dfc8be8652507c1a`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd361573e02e63c3a3c8445207e810b88509fd90e272b488b3fac80304b5b1f`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8015c1070d96733e69318a94355a7640dad8526a40678f924508af2bf023a2af`  
		Last Modified: Fri, 18 Apr 2025 03:17:19 GMT  
		Size: 294.5 MB (294456803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76294b70e11395a457780fca63b1b41dc5485a2ece93cae13a98b8ab22d30be`  
		Last Modified: Fri, 18 Apr 2025 03:16:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
