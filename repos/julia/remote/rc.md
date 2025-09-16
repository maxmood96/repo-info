## `julia:rc`

```console
$ docker pull julia@sha256:4d5ebc7108da6ae3eaf984779b989c66317820c0045e5c42f8adcd874fe7b86d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `julia:rc` - linux; amd64

```console
$ docker pull julia@sha256:277486a9b225e113a5e1e1c2683e3f8a96c17cb49b84aa0c907e33a3a2e59cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (321998841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217b4e36ba74dba4a69c679939fc0cf17875cf3a3a5947c493d14c049d350379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 23:59:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 08 Sep 2025 23:59:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_VERSION=1.12.0-rc2
# Mon, 08 Sep 2025 23:59:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc2-linux-x86_64.tar.gz'; 			sha256='ef2e16d4834390e5ec8dee4ba1e2dfee93747503ed45eab2c6eced9522ae1ba2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc2-linux-aarch64.tar.gz'; 			sha256='cfd710c716313b62c8fe320ae98f35b7b1d8dead94d6ffd4dfccf56e81a4e820'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc2-linux-i686.tar.gz'; 			sha256='24189244e5fe8f3a6cb7d5717efee638b37dd7fdf4d357c679f4f34c077cdbd4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 23:59:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a538028444bb6e2de8ad46d005f5239cc4cb6075971fa26097edaa3bb4d637a`  
		Last Modified: Wed, 10 Sep 2025 23:32:40 GMT  
		Size: 6.2 MB (6242794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d4ded67932b18a22718b1e750bde42bdb514779ff87618f5bdff9152a8ffb8`  
		Last Modified: Thu, 11 Sep 2025 03:03:40 GMT  
		Size: 286.0 MB (285982180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08ca063f4f01eb299ffac46d302f59029e011d090ab237e2fe0fd5de23849e1`  
		Last Modified: Wed, 10 Sep 2025 23:32:40 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:e37eb68e6c8c02d55e2c207a2393e237a79ac17103000d205566f593983203d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382e08c902294fc2abdd3af5dfe1164eec9dbf0e1c1201399f86105f6b139076`

```dockerfile
```

-	Layers:
	-	`sha256:1625c94ea5b5c617876a52d62207f1c3a646eed133c1053c7d5d300734b6639a`  
		Last Modified: Thu, 11 Sep 2025 02:02:48 GMT  
		Size: 2.2 MB (2239479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18d0a81de98f4131c2da3f1c6fae008d06a88bcc915e6727a8bb851049b35748`  
		Last Modified: Thu, 11 Sep 2025 02:02:49 GMT  
		Size: 17.2 KB (17218 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:bd8e93cdc0bd98b6588dec1c498bf11f4389ab916f7d1736f8841a5fa6827d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342512019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe07c28026b12ba1d9442a1c6ceb633e78a9207e35089b842757a3f43a56ecf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 23:59:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 08 Sep 2025 23:59:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_VERSION=1.12.0-rc2
# Mon, 08 Sep 2025 23:59:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc2-linux-x86_64.tar.gz'; 			sha256='ef2e16d4834390e5ec8dee4ba1e2dfee93747503ed45eab2c6eced9522ae1ba2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc2-linux-aarch64.tar.gz'; 			sha256='cfd710c716313b62c8fe320ae98f35b7b1d8dead94d6ffd4dfccf56e81a4e820'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc2-linux-i686.tar.gz'; 			sha256='24189244e5fe8f3a6cb7d5717efee638b37dd7fdf4d357c679f4f34c077cdbd4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 23:59:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb79b8d4fd1b21f70900905c6d0e25479d0f4d8fe9d49d4a795001abe9581c2`  
		Last Modified: Wed, 10 Sep 2025 23:34:51 GMT  
		Size: 6.2 MB (6153096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec56bf48766647c19d5c50c54cc8cb43b039e60ce24f2d0c5868e7a71b45d621`  
		Last Modified: Thu, 11 Sep 2025 19:18:33 GMT  
		Size: 306.2 MB (306221919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1567752f33b274be018bcaa6dd78f101850192628dfe4bb0538bc33e96e9af2a`  
		Last Modified: Wed, 10 Sep 2025 23:34:51 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:95c3ad52e8f083a7042ad81d4ab22f1f108c90977354bef865731df2379fb474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceebfe4dbf19c74ee4265f096352a54a8c1f0ef647f9e70e197b59454a785d24`

```dockerfile
```

-	Layers:
	-	`sha256:5e57d65712df9655fefbaac529cb0a6ed504872ab8dd935cbd235171e8949fe4`  
		Last Modified: Thu, 11 Sep 2025 02:02:52 GMT  
		Size: 2.2 MB (2239787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4050d544eec3105c15bcb0bed57bfca9d3a4e02f2ab085e10f7b7af4d9aa4056`  
		Last Modified: Thu, 11 Sep 2025 02:02:53 GMT  
		Size: 17.4 KB (17361 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:43ba4515079436460e6558924dd9106c476eb17eb64aa14367aba4960c69909e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267856164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94299d024bdc5db1e8e04f564823f77196727cc6fd907dca1651df223128fbf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 23:59:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 08 Sep 2025 23:59:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 08 Sep 2025 23:59:35 GMT
ENV JULIA_VERSION=1.12.0-rc2
# Mon, 08 Sep 2025 23:59:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.0-rc2-linux-x86_64.tar.gz'; 			sha256='ef2e16d4834390e5ec8dee4ba1e2dfee93747503ed45eab2c6eced9522ae1ba2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.0-rc2-linux-aarch64.tar.gz'; 			sha256='cfd710c716313b62c8fe320ae98f35b7b1d8dead94d6ffd4dfccf56e81a4e820'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.0-rc2-linux-i686.tar.gz'; 			sha256='24189244e5fe8f3a6cb7d5717efee638b37dd7fdf4d357c679f4f34c077cdbd4'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Sep 2025 23:59:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Sep 2025 23:59:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab5b4db3b0099aa1a38673b02fa4c3fb342d5f3c5e035eccb1baf04d8bfd31a`  
		Last Modified: Wed, 10 Sep 2025 23:32:37 GMT  
		Size: 6.4 MB (6427758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7048182fb6039c7ffc7a79445b8be04262f5868200da746093d1337d14224cd`  
		Last Modified: Tue, 16 Sep 2025 17:04:00 GMT  
		Size: 230.1 MB (230138256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7dcf5935c7cd1b4689fe8bc8f98cec4820ff9955b38f8a7638a9e271762185`  
		Last Modified: Wed, 10 Sep 2025 23:32:36 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:37904ceb1d4c222a1b5f7d8ab0d90e45809ecdfa5ffe23c5819aa1014cb2d0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9899d76badbd39cbb48acd60e97111ee62ab67a959ae6e58bd824da1857d794`

```dockerfile
```

-	Layers:
	-	`sha256:4b8ed230f61cc302aff5a064af2bf42186bdc74b97514feff5c0363e59c5b7aa`  
		Last Modified: Thu, 11 Sep 2025 02:02:57 GMT  
		Size: 2.2 MB (2236614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1747edc0ed00adc32c7e053f2a19027c97a69f2544ead02e9335145b67eaa62`  
		Last Modified: Thu, 11 Sep 2025 02:02:58 GMT  
		Size: 17.2 KB (17174 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - windows version 10.0.26100.6584; amd64

```console
$ docker pull julia@sha256:edd31c2109cf3448955c18bcec02fac0c26c1b32c8eb2bed1ea83e9ecad06ebe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3869370732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5eddcfda3cd4852e7757397550b9fb86ef4abdc3077895f512598fd8c36c116`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 23:36:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 23:36:04 GMT
ENV JULIA_VERSION=1.12.0-rc2
# Wed, 10 Sep 2025 23:36:05 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc2-win64.exe
# Wed, 10 Sep 2025 23:36:06 GMT
ENV JULIA_SHA256=955b26191bfbf30fedd6254c160a613068617c6da07b7a43729ae32584525079
# Wed, 10 Sep 2025 23:37:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 23:37:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d08eeaaaccb4330419698900f6d233fe0410546c547886c429c504efacb1fa6`  
		Last Modified: Wed, 10 Sep 2025 23:45:01 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08f6d365042bf6e8d4f68b2328683d786cc194e7d3f56ec0961312193758c36`  
		Last Modified: Wed, 10 Sep 2025 23:45:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1067283e8393ea35f9eaebf65fbc694dbe8c9af5a1f8d52e558587a2bda148`  
		Last Modified: Wed, 10 Sep 2025 23:45:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728bd7653ba666d8b1bbcb561b062fbcf40d7b4432e04c249d809e3b7ee2a80a`  
		Last Modified: Wed, 10 Sep 2025 23:45:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3868c58b4e2f27283371a466fdcfd087c6b2b01b1b418424ab9a546f11238b5`  
		Last Modified: Thu, 11 Sep 2025 02:05:48 GMT  
		Size: 297.9 MB (297924479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1d8d317527e14ed9de6bd9e134c9a0f34949660f6f3e3d9df7cbb86d3649d6`  
		Last Modified: Wed, 10 Sep 2025 23:45:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc` - windows version 10.0.20348.4171; amd64

```console
$ docker pull julia@sha256:e29ec595a17300fbd8f62b7f67441eb9598f5ea0840fbda8ebac8f191226315f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2580015733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2026341a568b656656ca39e7432fe13eb42f26d43170df1f0e87b57c20db05a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 23:33:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 23:33:14 GMT
ENV JULIA_VERSION=1.12.0-rc2
# Wed, 10 Sep 2025 23:33:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc2-win64.exe
# Wed, 10 Sep 2025 23:33:16 GMT
ENV JULIA_SHA256=955b26191bfbf30fedd6254c160a613068617c6da07b7a43729ae32584525079
# Wed, 10 Sep 2025 23:34:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Sep 2025 23:34:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f573c23280b839486c46bd56b45c9ba3b2131cd57989e6feecf23d28f9305c74`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d723fcf16e0e175cc22786d061369dc1fcf076cdac67843cb0da64d8db4846`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0528521d515504d283a8f45422b376607f78609f6dc72c2a3474bb211798a57b`  
		Last Modified: Wed, 10 Sep 2025 23:40:32 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c605b9244610637948e948316b3e61d5b793950fe304fb610057e3b18911927c`  
		Last Modified: Wed, 10 Sep 2025 23:40:33 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526eb8c03ff3abfece288651debc5ae0976ffd8ee9e828a6c64995d8a344c5f9`  
		Last Modified: Thu, 11 Sep 2025 02:05:26 GMT  
		Size: 297.9 MB (297864173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9da8cf4f9520a37ef6f179fedde7571a322fc594fc1d0b577f4ffe41649e148`  
		Last Modified: Wed, 10 Sep 2025 23:40:33 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
