## `julia:rc`

```console
$ docker pull julia@sha256:3df833ba09feb840477da184579654a7a554357a9c29b3255d462288b3ff54c7
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
$ docker pull julia@sha256:8f0aab328d5412ba0024b3619606bb7b4862366ebd20db820018c4bc7fa95bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344822920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3a3b1f0f7cdfaa07a19668766fb25dca30a328be434a9eea373b30805f88c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 17:42:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 17:42:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 17 Mar 2026 17:42:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 17:42:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 17 Mar 2026 17:42:41 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:42:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta3-linux-x86_64.tar.gz'; 			sha256='02111690b460ad1641d10fc920f3000a6254916d2f53b6d0f5f7482f47283e62'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta3-linux-i686.tar.gz'; 			sha256='3f0f1a362e611559b58acb71a50a130b9fc53273d157755cb7ac8f0fa7d99ef2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta3-linux-aarch64.tar.gz'; 			sha256='56043f2572c169a4d515b201f192d91792b4f5dfc8f1d90f595101a240693348'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 17 Mar 2026 17:42:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 17:42:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 17:42:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2b27ca88eb13c2672aaeb0babb2f004ee1bf8d51335c48db35fd6fcd23b9a9`  
		Last Modified: Tue, 17 Mar 2026 17:43:27 GMT  
		Size: 6.2 MB (6247038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116be04441d0f2aaa1a6690b508100ae18bbbc973440f23edfef1ead0c4d7978`  
		Last Modified: Tue, 17 Mar 2026 17:43:34 GMT  
		Size: 308.8 MB (308800010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a09f7290ac5efbe5e10f57b923d6e96cf3bffca824596fed498eb9721169b8`  
		Last Modified: Tue, 17 Mar 2026 17:43:27 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:d05f1d43b0507d7e8311dde5b3ad7f4439d4f6fb15cd0ca4ea401985daf6a725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ae7be4be767236df7d01a6cf2c0410246a65a37dba045a8030596009d37706`

```dockerfile
```

-	Layers:
	-	`sha256:2105e0429e48c017c31ab480d90dd70bfd652b27c287d0edeab91c43a90b3c7f`  
		Last Modified: Tue, 17 Mar 2026 17:43:27 GMT  
		Size: 2.2 MB (2240915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f8b8829abfa97310016c09738f93a3a834d148ef60d7110109997cb04dc86e`  
		Last Modified: Tue, 17 Mar 2026 17:43:27 GMT  
		Size: 17.2 KB (17189 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:82a1a4e4e9aba36f203836ef1d834f62ee835961b2d20d765f16658f95666573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.1 MB (369134902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921b6292144885fc6165bce348e2f58677b7062371e53101bac73102bb6368cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 17:41:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 17:41:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 17 Mar 2026 17:41:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 17:41:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 17 Mar 2026 17:41:48 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:41:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta3-linux-x86_64.tar.gz'; 			sha256='02111690b460ad1641d10fc920f3000a6254916d2f53b6d0f5f7482f47283e62'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta3-linux-i686.tar.gz'; 			sha256='3f0f1a362e611559b58acb71a50a130b9fc53273d157755cb7ac8f0fa7d99ef2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta3-linux-aarch64.tar.gz'; 			sha256='56043f2572c169a4d515b201f192d91792b4f5dfc8f1d90f595101a240693348'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 17 Mar 2026 17:41:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 17:41:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 17:41:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34543f75514eb60e59661f88320657a6e162c028a9836db7886d73fa18fc279f`  
		Last Modified: Tue, 17 Mar 2026 17:42:35 GMT  
		Size: 6.2 MB (6154435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c270a2190fa0bbf0e885b6363eda67771d9ad6fb1c522e7b77d5b115b03114`  
		Last Modified: Tue, 17 Mar 2026 17:42:41 GMT  
		Size: 332.8 MB (332841682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdafb05cf4d613f7e6b0534a1d6569e1f6fdaa741cf77d21bb4a6242ce47453d`  
		Last Modified: Tue, 17 Mar 2026 17:42:35 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:dd4538d7d4bf1cc64744672dd5d8948450a91799184745f747b1a5055e22c1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab5baaaaaca01f40579dc31e5453013093128a99fcca325311251586c09c586`

```dockerfile
```

-	Layers:
	-	`sha256:a017dae93aec84753ecb78d41c0fba7c5dc6346d3b709a2b3a55c7b4962f2557`  
		Last Modified: Tue, 17 Mar 2026 17:42:35 GMT  
		Size: 2.2 MB (2241223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8197792eaedb596aa0cdaac33e6ff13ed666370e17de4819e9f7a2fc1e90de1e`  
		Last Modified: Tue, 17 Mar 2026 17:42:35 GMT  
		Size: 17.3 KB (17332 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:rc` - linux; 386

```console
$ docker pull julia@sha256:cfc89377f654bbbec817db77f86520eaa7f0ade4a49e423229e340d46c5a52ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280483193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7af231e0beb9de594e2f750e5a1e1aec38f856aaae40a33ab618391ff86fbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 17:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 17:41:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 17 Mar 2026 17:41:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 17:41:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 17 Mar 2026 17:41:46 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:41:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.13/julia-1.13.0-beta3-linux-x86_64.tar.gz'; 			sha256='02111690b460ad1641d10fc920f3000a6254916d2f53b6d0f5f7482f47283e62'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.13/julia-1.13.0-beta3-linux-i686.tar.gz'; 			sha256='3f0f1a362e611559b58acb71a50a130b9fc53273d157755cb7ac8f0fa7d99ef2'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.13/julia-1.13.0-beta3-linux-aarch64.tar.gz'; 			sha256='56043f2572c169a4d515b201f192d91792b4f5dfc8f1d90f595101a240693348'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 17 Mar 2026 17:41:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 17:41:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 17:41:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e923377113450f48a8d461ae15182ff3fd82a770168a5160cadd8544c5a3e1`  
		Last Modified: Tue, 17 Mar 2026 17:42:23 GMT  
		Size: 6.4 MB (6433708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c400d700e7b9de53186aa262e78a07fd12c499215a24d38e6e81f53e0d6d7172`  
		Last Modified: Tue, 17 Mar 2026 17:42:27 GMT  
		Size: 242.8 MB (242757983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7566419e1905162fd1984c36f56e75e246140199a12976913248f3ca9e63b5`  
		Last Modified: Tue, 17 Mar 2026 17:42:22 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:rc` - unknown; unknown

```console
$ docker pull julia@sha256:5ce1fafdcae89d09fd88e72c31c8c15ab1e1d70dc40a4305cf0b915931918821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bddfd10be66f99bdf8d9309d77160825a8d31bc65e213460d83b4d3b94c811a`

```dockerfile
```

-	Layers:
	-	`sha256:f11c377908d26733278469fc9b426acb73de2e5dba9dc0af6d4db8e4b61dbbd4`  
		Last Modified: Tue, 17 Mar 2026 17:42:22 GMT  
		Size: 2.2 MB (2238050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2beac5184dedf5ceac20eb27a4f2f8b37fd34a12e027dbed0162a9ad66804dc`  
		Last Modified: Tue, 17 Mar 2026 17:42:22 GMT  
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
