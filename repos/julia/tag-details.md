<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `julia`

-	[`julia:1`](#julia1)
-	[`julia:1-bookworm`](#julia1-bookworm)
-	[`julia:1-trixie`](#julia1-trixie)
-	[`julia:1-windowsservercore`](#julia1-windowsservercore)
-	[`julia:1-windowsservercore-ltsc2022`](#julia1-windowsservercore-ltsc2022)
-	[`julia:1-windowsservercore-ltsc2025`](#julia1-windowsservercore-ltsc2025)
-	[`julia:1.10`](#julia110)
-	[`julia:1.10-alpine`](#julia110-alpine)
-	[`julia:1.10-alpine3.21`](#julia110-alpine321)
-	[`julia:1.10-alpine3.22`](#julia110-alpine322)
-	[`julia:1.10-bookworm`](#julia110-bookworm)
-	[`julia:1.10-trixie`](#julia110-trixie)
-	[`julia:1.10-windowsservercore`](#julia110-windowsservercore)
-	[`julia:1.10-windowsservercore-ltsc2022`](#julia110-windowsservercore-ltsc2022)
-	[`julia:1.10-windowsservercore-ltsc2025`](#julia110-windowsservercore-ltsc2025)
-	[`julia:1.10.10`](#julia11010)
-	[`julia:1.10.10-alpine`](#julia11010-alpine)
-	[`julia:1.10.10-alpine3.21`](#julia11010-alpine321)
-	[`julia:1.10.10-alpine3.22`](#julia11010-alpine322)
-	[`julia:1.10.10-bookworm`](#julia11010-bookworm)
-	[`julia:1.10.10-trixie`](#julia11010-trixie)
-	[`julia:1.10.10-windowsservercore`](#julia11010-windowsservercore)
-	[`julia:1.10.10-windowsservercore-ltsc2022`](#julia11010-windowsservercore-ltsc2022)
-	[`julia:1.10.10-windowsservercore-ltsc2025`](#julia11010-windowsservercore-ltsc2025)
-	[`julia:1.11`](#julia111)
-	[`julia:1.11-bookworm`](#julia111-bookworm)
-	[`julia:1.11-trixie`](#julia111-trixie)
-	[`julia:1.11-windowsservercore`](#julia111-windowsservercore)
-	[`julia:1.11-windowsservercore-ltsc2022`](#julia111-windowsservercore-ltsc2022)
-	[`julia:1.11-windowsservercore-ltsc2025`](#julia111-windowsservercore-ltsc2025)
-	[`julia:1.11.7`](#julia1117)
-	[`julia:1.11.7-bookworm`](#julia1117-bookworm)
-	[`julia:1.11.7-trixie`](#julia1117-trixie)
-	[`julia:1.11.7-windowsservercore`](#julia1117-windowsservercore)
-	[`julia:1.11.7-windowsservercore-ltsc2022`](#julia1117-windowsservercore-ltsc2022)
-	[`julia:1.11.7-windowsservercore-ltsc2025`](#julia1117-windowsservercore-ltsc2025)
-	[`julia:1.12`](#julia112)
-	[`julia:1.12-bookworm`](#julia112-bookworm)
-	[`julia:1.12-trixie`](#julia112-trixie)
-	[`julia:1.12-windowsservercore`](#julia112-windowsservercore)
-	[`julia:1.12-windowsservercore-ltsc2022`](#julia112-windowsservercore-ltsc2022)
-	[`julia:1.12-windowsservercore-ltsc2025`](#julia112-windowsservercore-ltsc2025)
-	[`julia:1.12.1`](#julia1121)
-	[`julia:1.12.1-bookworm`](#julia1121-bookworm)
-	[`julia:1.12.1-trixie`](#julia1121-trixie)
-	[`julia:1.12.1-windowsservercore`](#julia1121-windowsservercore)
-	[`julia:1.12.1-windowsservercore-ltsc2022`](#julia1121-windowsservercore-ltsc2022)
-	[`julia:1.12.1-windowsservercore-ltsc2025`](#julia1121-windowsservercore-ltsc2025)
-	[`julia:bookworm`](#juliabookworm)
-	[`julia:latest`](#julialatest)
-	[`julia:trixie`](#juliatrixie)
-	[`julia:windowsservercore`](#juliawindowsservercore)
-	[`julia:windowsservercore-ltsc2022`](#juliawindowsservercore-ltsc2022)
-	[`julia:windowsservercore-ltsc2025`](#juliawindowsservercore-ltsc2025)

## `julia:1`

```console
$ docker pull julia@sha256:6988944c178fa71f4fb0548281fc6dc5c454a3231021d0f3f3c7b1b98a7be136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:3aae05f9821c507b842d87ce7a83725c4467edaf4d4ae3bf623b8ff07004b05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:500372ec6ab9741301c27e345cc7e6708946b36de0216c3b3e6239a163c9b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5997a30c10df568c491bbe08a95a45b19abeb886af268909f72ffdeef3f22a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ace6d66d3a3d6fad5a1bd31565e9c119574e312dbf2c55d7ced0a4d992e9`  
		Last Modified: Tue, 04 Nov 2025 00:18:36 GMT  
		Size: 5.7 MB (5716426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d378682861b91f1053d2a1d43464b2e57b6395f94b5f3616162773b305beb7a`  
		Last Modified: Tue, 04 Nov 2025 10:36:01 GMT  
		Size: 289.5 MB (289470929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b061c9f75eba30cf7b20f413cee1eb00a9792af624a81cc98ae89703a73af6f`  
		Last Modified: Tue, 04 Nov 2025 00:18:35 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0f2ade0b8ea9e16026159dd251a169c750b2036fadf23fa790173f5786abef5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca9af7418798601cc04f6d6a48739a9a5da2a2e8482a07a023fdcf69ec0087`

```dockerfile
```

-	Layers:
	-	`sha256:a1ca6642d24f5181480f5bb0515421c6f570b5abdbe45693da59426dc16c0569`  
		Last Modified: Tue, 04 Nov 2025 09:03:26 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f2b8bfcd164157a77616ff0c66cd57015fb0f62d644a857a0f0afae188278b`  
		Last Modified: Tue, 04 Nov 2025 09:03:27 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4dfad4c810fdc31ae725d248983cbefbae1df3f6bdb6b4e944002a94a68c36bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06ec30bbfc55e57787d9f31eca6b80846748ef0363c4f9fcfe81df203ef0ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7199a6c929b6d0910d53e32159d8d4a96b2bbfe63afacda8c1e08bb035462`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 5.6 MB (5567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05efc5faad78e038dbe03bd02c615e0b76965f7a8a490e504f4ce7d87b612e`  
		Last Modified: Tue, 04 Nov 2025 00:18:39 GMT  
		Size: 310.2 MB (310205326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47e0b771b47e33a97f9e83589db5a6704058ee4a6d0ebb2ea3a58608487de5`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b9e05a0cbe438b70a93dad310acf8080004bb3a3f8711d4e8bcc09dbccb5a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393cbcc803f86aaa5f4ca3e66fd98503eff8f9899ec570fa2a2ab4b339456db6`

```dockerfile
```

-	Layers:
	-	`sha256:1489217e1ad8fa0212b331b460f9a9d4179d0e0f91f2678e1584d337977e1ed8`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdd4101aa2f92fb683b0ade00736d7f9febb97dbdc1620c2437587dde528473`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b7b2aa64a703e070f3336775ca69c137d785eb8700ae65f77cc0e6b759ee5d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312d4d17eebcf8fa147335c9eb1528fb268c227023f969103062ea8fe0c5830f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed679b54c5167ee52acb091f4d82f3b6acbafe02cddb714ebae4a0595a28f4`  
		Last Modified: Tue, 04 Nov 2025 00:17:28 GMT  
		Size: 5.9 MB (5878102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c583711dbb5e1bcb432195e396db5b8c27f36cd377de394faa956eeafaef9c9`  
		Last Modified: Tue, 04 Nov 2025 00:17:14 GMT  
		Size: 231.0 MB (231003092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c81c730697f6e563baad7c504576c729ef56d9082d11989882c45b83572fc2`  
		Last Modified: Tue, 04 Nov 2025 00:17:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:590ef71cd93f47132cdb712b908065edb792a5d2740d059f9f901bff40f74e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7354b4e55ca63d4fd0ac996a59834e68b1bbee3310e2b7777d6a6693583b56f5`

```dockerfile
```

-	Layers:
	-	`sha256:5dbc38afd08e09a5287ae9337d8aac4c769864909ee65694125473f54b9ee8fc`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5546efb59869a678415785da134451168dcd6768ff70c4cd0481388882aecd5b`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-trixie`

```console
$ docker pull julia@sha256:ac48e8257c839954341858486babc1e1ec1ec61c137577dba475a4de1bcf257c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:37c56bf72faa4943f68f85317d46d634b09f9f80d8eb60a56c5b43a4a10ef152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1373ec157b80534a185f04456f792e25f678f6fd3ba7c1c90e5df512f1d6eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fa10c1c8c32867203dde7a7be57b7e184bda0c46e4bfd0fa4054e4abd8ca9d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:b0e384dfa78088325e0aeab5cfe66cdc9f2062fc22e30932451f9845f3c78dd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:0be1836fe29b84a81a3f2392499be0f1f19c4aaba202b4503236a853d2c0bdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7241add4df9b1f679f3bba4863c0fd58aa7e854b0c5c191b90755d1730539cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:06:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 04:06:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:06:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d74ee65a5c8887d4e897ad989f11f0bcb62ac7d2366e03e4d3ed724098c6f9`  
		Last Modified: Tue, 04 Nov 2025 04:06:50 GMT  
		Size: 6.2 MB (6242791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd14cb66cc421efef6c3fc4e502fd4f14ed34b531bfa9b946175248f8d1457`  
		Last Modified: Tue, 04 Nov 2025 09:29:48 GMT  
		Size: 176.4 MB (176362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d063ea66e0ed144e5d9961751f21aa086e38f006ed44b8ffc92457cb43d3f4`  
		Last Modified: Tue, 04 Nov 2025 04:06:49 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:1c90a143de00756516f02bf7f4ad670b4a85d2ef7b78eacf9929d6f8658c5b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578816bd108370e2ee32c28f6037aa88efa133e3c9f498b49e73a2de57e96728`

```dockerfile
```

-	Layers:
	-	`sha256:783cad2d993fc11df084756d4ccf86ec7a818d3b9f352da4e1acb6bbf8be3284`  
		Last Modified: Tue, 04 Nov 2025 09:02:24 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ab0badf666ea173f8c9198febcc7bf3be71d34dffca9fa4ebc6d5e1dda07ce`  
		Last Modified: Tue, 04 Nov 2025 09:02:25 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9034543a863fa5fc83a8c69b7184f76407be8c11175f7755e8c62999622bf30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213746025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5054084ef14e78af405d41a58123fa0216271b8d270ac19eb938e6582e7c64fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860a1cc05c2a5182c3ec611330be4e7f8a4c3614cd9c6fc64939f840fe39b922`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 6.2 MB (6153088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd484f8a8c3f57b03b0dde9fbb6287c235f5c2653c66d13c4633d32e4e0169a3`  
		Last Modified: Tue, 04 Nov 2025 01:20:39 GMT  
		Size: 177.5 MB (177450266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d256230749ee4d70eb88e530866c8bf1253a3357a5aa6011e17147806ad8a9d`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:0cdd53a235d899ab26f0c20cabbf1efe2cc48c674192f8bafbee32df5f667201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ef3c90a2821939161b2950600b3d5816b697f05e1532322ee2578c4f52c76d`

```dockerfile
```

-	Layers:
	-	`sha256:c4398e34af44927e8155eafa68eb073a99ed6cfa72d627792f13955a0957e572`  
		Last Modified: Tue, 04 Nov 2025 12:02:43 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdeb45a064847163ddeb413336129bf867d70ca72df0a108051a8038638d2b5`  
		Last Modified: Tue, 04 Nov 2025 12:02:44 GMT  
		Size: 17.3 KB (17286 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:e423563d8d90d8de959bc69db5b809d77585d80edc7ac937d43931c64bab6608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ffdd11d10ae385984d8501a7a11622fd3265ac316188a775ecfb5d6dc85f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9aeb3401bd2d24090ebce607bb50fbc32e48f39c0a9293e5a98af40be3141`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 6.4 MB (6427758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b334668a8683483982a48e9af66fe679c9746cd98e0a3588db6b5f9e5cfd779`  
		Last Modified: Tue, 04 Nov 2025 01:20:27 GMT  
		Size: 157.8 MB (157841776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6d0c4617c43fd875c9e587f50ae36b4ffb5519cae63ed329bf009cdeae2c3`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:2891e0bd4ec4a6f4294f4c88edee7cf05ecfc3ebb3c188c6889d4ac6fb5ba8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3f0e4f385ef87fcf0c92eda1160d601a585513182bc8df78ac4f731cb2c44`

```dockerfile
```

-	Layers:
	-	`sha256:11bd16cd6a5af46bf23b9e389a3da58347e894fd75ac31bd79639b6ddca2e8b0`  
		Last Modified: Tue, 04 Nov 2025 12:02:47 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7a63328180c5d7a2e69d92179f82b64dbcf17de8dcf8c719d2b4cebb2a400b7`  
		Last Modified: Tue, 04 Nov 2025 12:02:48 GMT  
		Size: 17.1 KB (17134 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; ppc64le

```console
$ docker pull julia@sha256:34d9137560b8a388693b28f459d724687334b78f8870877694eb3c169ce669ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef672dde653052764643aaaf988bd53503470b382112a62899b3b2acbe462f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:49:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:49:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b5bae0acc51d0467ea809a87487fb9a5be6888a52db6d14563676c8ce8fa3c`  
		Last Modified: Tue, 04 Nov 2025 01:50:02 GMT  
		Size: 155.4 MB (155388117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a2291d082e640ce187f7c09d19695b942b2bbff7a670fd9392b7dcb86fb17b`  
		Last Modified: Tue, 04 Nov 2025 01:50:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:985fefaed90ae4275bd3498273d2b5bff0c68073ade0a24987505b210ac4337d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bedc4fa09680d44ab78532c8ec4c17c6164440a10ebf591a7960381debe3401`

```dockerfile
```

-	Layers:
	-	`sha256:c73dbdc04a315b11f8e04ac9f6d42e4a08def6925be0b71246bb36ccc0923bf2`  
		Last Modified: Tue, 04 Nov 2025 09:02:36 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27665359883bca78e432dfbaf04d6aad9ba8830c21d325b20d1fa9987e196944`  
		Last Modified: Tue, 04 Nov 2025 09:02:37 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e91781bb5c75b68df73f8dddcbe5d0b8bd7ab8886d556e9dd6a5bc57e249bf22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409148875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ce5fc2e06dcbdcd7d6447aa3f34194b771307373c175165d0ca7421ee6d3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7597b32b86f33d6cfe1536df796fc6ad77a63b0669d9f0f90ba38d5485891baa`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570728235470284f5444d9ae662ec0ae42d0fccc593389c9aba70d180166829`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198872149605ccef2bc20a708965178952a163fc95f8ed11419cc298c8b14cdb`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672c735e2472c8fa62a4f46f39518b8c0dffb6f261f1d9a1710ae08300e7ee9`  
		Last Modified: Fri, 24 Oct 2025 20:03:18 GMT  
		Size: 188.8 MB (188795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8001eb9d6f76ebb7d37099515e9ab0b040cbd0c46858de0a55ff98651a863`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:5e0bf498d04d76afae3343d9e9fc06cfc4e3ab0ad97e0f1d01cf65d8eac588be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766121325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e922d9ab00a0c2ad8f861df765bf0bce0e6afb5cd8e20d1494d600b708a4782`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:03 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:11:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:11:05 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:13:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49096beec96dd6d9b8b02ecc62cb846825eb45de97ab036485e13e3eb5d808fe`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6b457c4fbfcbdf61ab708c862ff837a7fc331fff6df5dac7075f5ce1be901`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d762a60280ee7c3798a5e61b737e41026a6f6cf3a47a1a612224ae52b9152`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a8f91cd7872519b244ce28b3ad3e5def0b9a34e53237536890d2a19d700060`  
		Last Modified: Fri, 24 Oct 2025 20:03:13 GMT  
		Size: 188.9 MB (188921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f795e174a6876adc6451536991eff371fc61e619c8a6395a0c4ca646df53`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-alpine`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.21`

```console
$ docker pull julia@sha256:d1a3e070ace2a47e5eb3cf2e507a090c9b0be78e986d61fa40b7b708e53a3842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:52ac97bc4b7d2863b731985c6614a46e6ab4f13f13f3c8d91d933a5c13055102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181941938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df008c40538a112568d8ff3054242fbabee9d18edd7f08445c7c38cf6f7cea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bda53ebb21b1322cf919f16ba5b28ae9b1d9acd8c0d0da1518623793417c9`  
		Last Modified: Sat, 11 Oct 2025 01:40:30 GMT  
		Size: 178.3 MB (178298998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d772ec346b861be7ae3ae4939fab2ea82732b66bf0931f5d9a7cb217646c0c6`  
		Last Modified: Wed, 08 Oct 2025 23:29:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:9b1b7279a096a1493387b3ed071e6f6201a78ed8dfd3ecc09596e34b48a8e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a9169be517a413e716324eb64afaf1e70b5e4bf29b7ab8205696d41c42cfd`

```dockerfile
```

-	Layers:
	-	`sha256:d87cc8698e0b72551245a2ae783ddb2d064e0bf0c6a2b90e877668ed5777c209`  
		Last Modified: Thu, 09 Oct 2025 02:02:25 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b3221cfc383c0844d2d950de60a17caa749b9d059d4a7e43848dc1f00be791`  
		Last Modified: Thu, 09 Oct 2025 02:02:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-alpine3.22`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-bookworm`

```console
$ docker pull julia@sha256:45bc4dbc25e99e4b1627d875a0bda9ecaed7594eaf2e912063716b1362fda24e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:4bda83dd9a39110c47872fbd25d5057c3047dc8abb9d6b35a4ecfffdc8b658fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604899d2fa1050f182d1ae5bdd15c2139e2e41a41de28b1047db8ec9ab5ef848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:18:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:18:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:18:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:18:51 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 00:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:18:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ace6d66d3a3d6fad5a1bd31565e9c119574e312dbf2c55d7ced0a4d992e9`  
		Last Modified: Tue, 04 Nov 2025 00:18:36 GMT  
		Size: 5.7 MB (5716426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da679be7402174d1185b0f17606b867b98643f73c7cc95dad0b2e16e00e91aa7`  
		Last Modified: Tue, 04 Nov 2025 09:17:33 GMT  
		Size: 176.3 MB (176324335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ec3b59508703ca5638df6b1d2ccb4ed5dfca4f8f5b3953902996e63a9752af`  
		Last Modified: Tue, 04 Nov 2025 00:19:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:40296d09536d5f80ac4ed2eccc4049db6cf1491bd847556f10ebd7f36116282c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a33f7225ff743e63ef62a204c797d11c5a29efdcb08c8965634d8d26976e27`

```dockerfile
```

-	Layers:
	-	`sha256:f4aef0138ce6bbc8ea4da422c1c364780680423a81a060249c4f7cb9bf45d403`  
		Last Modified: Tue, 04 Nov 2025 09:02:34 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0686819fa2a869291ce7e8dc1fcb09fae37060d173cd79a20b1de8844add2377`  
		Last Modified: Tue, 04 Nov 2025 09:02:34 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1ec42c0c95b1341e44e12c2695533d415cd2be98d56220e9b4642e76a1df6f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c107bfdd9769f8548f754a55d66e3d432102dcdb9aa2974ef66a28c05a6bc6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:19:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:19:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:19:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:19:01 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 00:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:19:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:19:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7199a6c929b6d0910d53e32159d8d4a96b2bbfe63afacda8c1e08bb035462`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 5.6 MB (5567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611c49edecb508eb5b7510f801fee4729fcfb600b2b73b6db6be2f2f0365dab4`  
		Last Modified: Tue, 04 Nov 2025 00:19:34 GMT  
		Size: 177.4 MB (177412350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55bcc1527376498bd93e948c85f62591d0492f5bb15eeda78d20ab142059d63`  
		Last Modified: Tue, 04 Nov 2025 00:19:40 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:87a8730a90649d840d5f24ae412f951e490000dd220f1989fa1695182997034d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73ad65d708f63b3872a16d44e8c018aaf7edcec65ab54368c5c96c676f44319`

```dockerfile
```

-	Layers:
	-	`sha256:f569c5c87967337d10be32d568c5ac44fc56c4b88402a058bd81df78d420e4d0`  
		Last Modified: Tue, 04 Nov 2025 12:02:52 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5cab54a5a58f38337b3daee8c455212d5897c346f28d803bada61596cd8cbd5`  
		Last Modified: Tue, 04 Nov 2025 12:02:53 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:3f8a03007a027f5f20513ee68ebd0a4914c1a915322ae87a32a0a3e018b38cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd0a2d4c889e7762ae48f4c42cf198a6a38e1b63252ecb73f5efb24619edbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:36 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 00:16:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e53a671270cfb23b9ecd0c61dfb767438f7bd0aa02c20b42ced4ecbf32a253`  
		Last Modified: Tue, 04 Nov 2025 00:17:09 GMT  
		Size: 5.9 MB (5878028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e10bc4e2aeed2fb8b6386054cb6547de65c096b7bc6c6cb836c643d8d685a4`  
		Last Modified: Tue, 04 Nov 2025 00:17:03 GMT  
		Size: 157.8 MB (157807873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae666ec88791443865c71578b87e96283e5411ccd94556d767edd2c310e1929f`  
		Last Modified: Tue, 04 Nov 2025 00:17:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9911c0cf4f0835c4a0c063bb70e1140e14346b1a06f8675631dce10b3dc28c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd660a1b3cd0cc5ff60569943183acbdce5ca4c6a731ccfb6c4f5ee20f28035d`

```dockerfile
```

-	Layers:
	-	`sha256:3d673b10015287f5de9c3c019a35ec5369e0c1b68fa12329a2344b62f3c59a70`  
		Last Modified: Tue, 04 Nov 2025 12:02:57 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918cb1649ded3944e7056193f9e0bda5bbd02a3d20b2558fea3a1d963c55689c`  
		Last Modified: Tue, 04 Nov 2025 12:02:58 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:49ad9e9a851899eae8db8a17307e95d55cc252ca3115e708e6c22cf5d16f29eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6492624703a3f7d8b9062f3f6cf47e9b81088f95b8e653693f283a5627c5dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:51:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:51:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:51:01 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:51:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:51:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:51:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:51:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100319a5fe2f62c408488b2652211045c6a4b819d76492b9ffce2f37abb9ba00`  
		Last Modified: Tue, 04 Nov 2025 01:48:02 GMT  
		Size: 6.3 MB (6256339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3923a442c8b8de51892aacbd2e260437a31b5d25e44fa1272bc7b7d882050235`  
		Last Modified: Tue, 04 Nov 2025 01:52:00 GMT  
		Size: 155.4 MB (155354872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f666d81055dddc17b4e4dea946788cea14b6835875e87b6ee934c072f207841`  
		Last Modified: Tue, 04 Nov 2025 01:52:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:baa9c4c07f62fe7eadc751e107b67d8e0371c7a99682f9228f71f9d82edd9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0275c7ea898dc2ec596c40d092455f811b73c995e90fed1e5fc9efa4f7e541`

```dockerfile
```

-	Layers:
	-	`sha256:3e2bbb0dea0422671dfbd677f0bdf76d17779b3f4339d0ca0637092f34f335c6`  
		Last Modified: Tue, 04 Nov 2025 09:02:45 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5312dfccac519202c283edee182da0b928b65aba35e434e5bf49819d90593fd8`  
		Last Modified: Tue, 04 Nov 2025 09:02:45 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-trixie`

```console
$ docker pull julia@sha256:6e8a24f3468fa547cd15dd2a570b18083fc3e34b70bfc02f220aedf8c5064df6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10-trixie` - linux; amd64

```console
$ docker pull julia@sha256:0be1836fe29b84a81a3f2392499be0f1f19c4aaba202b4503236a853d2c0bdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7241add4df9b1f679f3bba4863c0fd58aa7e854b0c5c191b90755d1730539cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:06:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 04:06:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:06:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d74ee65a5c8887d4e897ad989f11f0bcb62ac7d2366e03e4d3ed724098c6f9`  
		Last Modified: Tue, 04 Nov 2025 04:06:50 GMT  
		Size: 6.2 MB (6242791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd14cb66cc421efef6c3fc4e502fd4f14ed34b531bfa9b946175248f8d1457`  
		Last Modified: Tue, 04 Nov 2025 09:29:48 GMT  
		Size: 176.4 MB (176362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d063ea66e0ed144e5d9961751f21aa086e38f006ed44b8ffc92457cb43d3f4`  
		Last Modified: Tue, 04 Nov 2025 04:06:49 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1c90a143de00756516f02bf7f4ad670b4a85d2ef7b78eacf9929d6f8658c5b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578816bd108370e2ee32c28f6037aa88efa133e3c9f498b49e73a2de57e96728`

```dockerfile
```

-	Layers:
	-	`sha256:783cad2d993fc11df084756d4ccf86ec7a818d3b9f352da4e1acb6bbf8be3284`  
		Last Modified: Tue, 04 Nov 2025 09:02:24 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ab0badf666ea173f8c9198febcc7bf3be71d34dffca9fa4ebc6d5e1dda07ce`  
		Last Modified: Tue, 04 Nov 2025 09:02:25 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9034543a863fa5fc83a8c69b7184f76407be8c11175f7755e8c62999622bf30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213746025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5054084ef14e78af405d41a58123fa0216271b8d270ac19eb938e6582e7c64fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860a1cc05c2a5182c3ec611330be4e7f8a4c3614cd9c6fc64939f840fe39b922`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 6.2 MB (6153088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd484f8a8c3f57b03b0dde9fbb6287c235f5c2653c66d13c4633d32e4e0169a3`  
		Last Modified: Tue, 04 Nov 2025 01:20:39 GMT  
		Size: 177.5 MB (177450266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d256230749ee4d70eb88e530866c8bf1253a3357a5aa6011e17147806ad8a9d`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:0cdd53a235d899ab26f0c20cabbf1efe2cc48c674192f8bafbee32df5f667201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ef3c90a2821939161b2950600b3d5816b697f05e1532322ee2578c4f52c76d`

```dockerfile
```

-	Layers:
	-	`sha256:c4398e34af44927e8155eafa68eb073a99ed6cfa72d627792f13955a0957e572`  
		Last Modified: Tue, 04 Nov 2025 12:02:43 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdeb45a064847163ddeb413336129bf867d70ca72df0a108051a8038638d2b5`  
		Last Modified: Tue, 04 Nov 2025 12:02:44 GMT  
		Size: 17.3 KB (17286 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:e423563d8d90d8de959bc69db5b809d77585d80edc7ac937d43931c64bab6608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ffdd11d10ae385984d8501a7a11622fd3265ac316188a775ecfb5d6dc85f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9aeb3401bd2d24090ebce607bb50fbc32e48f39c0a9293e5a98af40be3141`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 6.4 MB (6427758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b334668a8683483982a48e9af66fe679c9746cd98e0a3588db6b5f9e5cfd779`  
		Last Modified: Tue, 04 Nov 2025 01:20:27 GMT  
		Size: 157.8 MB (157841776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6d0c4617c43fd875c9e587f50ae36b4ffb5519cae63ed329bf009cdeae2c3`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2891e0bd4ec4a6f4294f4c88edee7cf05ecfc3ebb3c188c6889d4ac6fb5ba8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3f0e4f385ef87fcf0c92eda1160d601a585513182bc8df78ac4f731cb2c44`

```dockerfile
```

-	Layers:
	-	`sha256:11bd16cd6a5af46bf23b9e389a3da58347e894fd75ac31bd79639b6ddca2e8b0`  
		Last Modified: Tue, 04 Nov 2025 12:02:47 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7a63328180c5d7a2e69d92179f82b64dbcf17de8dcf8c719d2b4cebb2a400b7`  
		Last Modified: Tue, 04 Nov 2025 12:02:48 GMT  
		Size: 17.1 KB (17134 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:34d9137560b8a388693b28f459d724687334b78f8870877694eb3c169ce669ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef672dde653052764643aaaf988bd53503470b382112a62899b3b2acbe462f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:49:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:49:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b5bae0acc51d0467ea809a87487fb9a5be6888a52db6d14563676c8ce8fa3c`  
		Last Modified: Tue, 04 Nov 2025 01:50:02 GMT  
		Size: 155.4 MB (155388117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a2291d082e640ce187f7c09d19695b942b2bbff7a670fd9392b7dcb86fb17b`  
		Last Modified: Tue, 04 Nov 2025 01:50:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:985fefaed90ae4275bd3498273d2b5bff0c68073ade0a24987505b210ac4337d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bedc4fa09680d44ab78532c8ec4c17c6164440a10ebf591a7960381debe3401`

```dockerfile
```

-	Layers:
	-	`sha256:c73dbdc04a315b11f8e04ac9f6d42e4a08def6925be0b71246bb36ccc0923bf2`  
		Last Modified: Tue, 04 Nov 2025 09:02:36 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27665359883bca78e432dfbaf04d6aad9ba8830c21d325b20d1fa9987e196944`  
		Last Modified: Tue, 04 Nov 2025 09:02:37 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-windowsservercore`

```console
$ docker pull julia@sha256:1621a74d40ee0b36a332a7f33bcefbb97c824db63e656ae6d7404fe653846166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e91781bb5c75b68df73f8dddcbe5d0b8bd7ab8886d556e9dd6a5bc57e249bf22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409148875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ce5fc2e06dcbdcd7d6447aa3f34194b771307373c175165d0ca7421ee6d3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7597b32b86f33d6cfe1536df796fc6ad77a63b0669d9f0f90ba38d5485891baa`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570728235470284f5444d9ae662ec0ae42d0fccc593389c9aba70d180166829`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198872149605ccef2bc20a708965178952a163fc95f8ed11419cc298c8b14cdb`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672c735e2472c8fa62a4f46f39518b8c0dffb6f261f1d9a1710ae08300e7ee9`  
		Last Modified: Fri, 24 Oct 2025 20:03:18 GMT  
		Size: 188.8 MB (188795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8001eb9d6f76ebb7d37099515e9ab0b040cbd0c46858de0a55ff98651a863`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:5e0bf498d04d76afae3343d9e9fc06cfc4e3ab0ad97e0f1d01cf65d8eac588be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766121325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e922d9ab00a0c2ad8f861df765bf0bce0e6afb5cd8e20d1494d600b708a4782`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:03 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:11:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:11:05 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:13:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49096beec96dd6d9b8b02ecc62cb846825eb45de97ab036485e13e3eb5d808fe`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6b457c4fbfcbdf61ab708c862ff837a7fc331fff6df5dac7075f5ce1be901`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d762a60280ee7c3798a5e61b737e41026a6f6cf3a47a1a612224ae52b9152`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a8f91cd7872519b244ce28b3ad3e5def0b9a34e53237536890d2a19d700060`  
		Last Modified: Fri, 24 Oct 2025 20:03:13 GMT  
		Size: 188.9 MB (188921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f795e174a6876adc6451536991eff371fc61e619c8a6395a0c4ca646df53`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9c6803f12356d3db735091ee7ac10cf1948f49c1ab0c3211cd81833d520f9936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:5e0bf498d04d76afae3343d9e9fc06cfc4e3ab0ad97e0f1d01cf65d8eac588be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766121325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e922d9ab00a0c2ad8f861df765bf0bce0e6afb5cd8e20d1494d600b708a4782`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:03 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:11:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:11:05 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:13:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49096beec96dd6d9b8b02ecc62cb846825eb45de97ab036485e13e3eb5d808fe`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6b457c4fbfcbdf61ab708c862ff837a7fc331fff6df5dac7075f5ce1be901`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d762a60280ee7c3798a5e61b737e41026a6f6cf3a47a1a612224ae52b9152`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a8f91cd7872519b244ce28b3ad3e5def0b9a34e53237536890d2a19d700060`  
		Last Modified: Fri, 24 Oct 2025 20:03:13 GMT  
		Size: 188.9 MB (188921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f795e174a6876adc6451536991eff371fc61e619c8a6395a0c4ca646df53`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:6150fe17c6457736dcfafe2d184e7f5f9bea7e44d25de1573bbbbdeb511c1f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e91781bb5c75b68df73f8dddcbe5d0b8bd7ab8886d556e9dd6a5bc57e249bf22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409148875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ce5fc2e06dcbdcd7d6447aa3f34194b771307373c175165d0ca7421ee6d3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7597b32b86f33d6cfe1536df796fc6ad77a63b0669d9f0f90ba38d5485891baa`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570728235470284f5444d9ae662ec0ae42d0fccc593389c9aba70d180166829`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198872149605ccef2bc20a708965178952a163fc95f8ed11419cc298c8b14cdb`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672c735e2472c8fa62a4f46f39518b8c0dffb6f261f1d9a1710ae08300e7ee9`  
		Last Modified: Fri, 24 Oct 2025 20:03:18 GMT  
		Size: 188.8 MB (188795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8001eb9d6f76ebb7d37099515e9ab0b040cbd0c46858de0a55ff98651a863`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10`

```console
$ docker pull julia@sha256:b0e384dfa78088325e0aeab5cfe66cdc9f2062fc22e30932451f9845f3c78dd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.10.10` - linux; amd64

```console
$ docker pull julia@sha256:0be1836fe29b84a81a3f2392499be0f1f19c4aaba202b4503236a853d2c0bdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7241add4df9b1f679f3bba4863c0fd58aa7e854b0c5c191b90755d1730539cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:06:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 04:06:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:06:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d74ee65a5c8887d4e897ad989f11f0bcb62ac7d2366e03e4d3ed724098c6f9`  
		Last Modified: Tue, 04 Nov 2025 04:06:50 GMT  
		Size: 6.2 MB (6242791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd14cb66cc421efef6c3fc4e502fd4f14ed34b531bfa9b946175248f8d1457`  
		Last Modified: Tue, 04 Nov 2025 09:29:48 GMT  
		Size: 176.4 MB (176362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d063ea66e0ed144e5d9961751f21aa086e38f006ed44b8ffc92457cb43d3f4`  
		Last Modified: Tue, 04 Nov 2025 04:06:49 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:1c90a143de00756516f02bf7f4ad670b4a85d2ef7b78eacf9929d6f8658c5b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578816bd108370e2ee32c28f6037aa88efa133e3c9f498b49e73a2de57e96728`

```dockerfile
```

-	Layers:
	-	`sha256:783cad2d993fc11df084756d4ccf86ec7a818d3b9f352da4e1acb6bbf8be3284`  
		Last Modified: Tue, 04 Nov 2025 09:02:24 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ab0badf666ea173f8c9198febcc7bf3be71d34dffca9fa4ebc6d5e1dda07ce`  
		Last Modified: Tue, 04 Nov 2025 09:02:25 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9034543a863fa5fc83a8c69b7184f76407be8c11175f7755e8c62999622bf30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213746025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5054084ef14e78af405d41a58123fa0216271b8d270ac19eb938e6582e7c64fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860a1cc05c2a5182c3ec611330be4e7f8a4c3614cd9c6fc64939f840fe39b922`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 6.2 MB (6153088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd484f8a8c3f57b03b0dde9fbb6287c235f5c2653c66d13c4633d32e4e0169a3`  
		Last Modified: Tue, 04 Nov 2025 01:20:39 GMT  
		Size: 177.5 MB (177450266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d256230749ee4d70eb88e530866c8bf1253a3357a5aa6011e17147806ad8a9d`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:0cdd53a235d899ab26f0c20cabbf1efe2cc48c674192f8bafbee32df5f667201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ef3c90a2821939161b2950600b3d5816b697f05e1532322ee2578c4f52c76d`

```dockerfile
```

-	Layers:
	-	`sha256:c4398e34af44927e8155eafa68eb073a99ed6cfa72d627792f13955a0957e572`  
		Last Modified: Tue, 04 Nov 2025 12:02:43 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdeb45a064847163ddeb413336129bf867d70ca72df0a108051a8038638d2b5`  
		Last Modified: Tue, 04 Nov 2025 12:02:44 GMT  
		Size: 17.3 KB (17286 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; 386

```console
$ docker pull julia@sha256:e423563d8d90d8de959bc69db5b809d77585d80edc7ac937d43931c64bab6608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ffdd11d10ae385984d8501a7a11622fd3265ac316188a775ecfb5d6dc85f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9aeb3401bd2d24090ebce607bb50fbc32e48f39c0a9293e5a98af40be3141`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 6.4 MB (6427758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b334668a8683483982a48e9af66fe679c9746cd98e0a3588db6b5f9e5cfd779`  
		Last Modified: Tue, 04 Nov 2025 01:20:27 GMT  
		Size: 157.8 MB (157841776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6d0c4617c43fd875c9e587f50ae36b4ffb5519cae63ed329bf009cdeae2c3`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:2891e0bd4ec4a6f4294f4c88edee7cf05ecfc3ebb3c188c6889d4ac6fb5ba8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3f0e4f385ef87fcf0c92eda1160d601a585513182bc8df78ac4f731cb2c44`

```dockerfile
```

-	Layers:
	-	`sha256:11bd16cd6a5af46bf23b9e389a3da58347e894fd75ac31bd79639b6ddca2e8b0`  
		Last Modified: Tue, 04 Nov 2025 12:02:47 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7a63328180c5d7a2e69d92179f82b64dbcf17de8dcf8c719d2b4cebb2a400b7`  
		Last Modified: Tue, 04 Nov 2025 12:02:48 GMT  
		Size: 17.1 KB (17134 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; ppc64le

```console
$ docker pull julia@sha256:34d9137560b8a388693b28f459d724687334b78f8870877694eb3c169ce669ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef672dde653052764643aaaf988bd53503470b382112a62899b3b2acbe462f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:49:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:49:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b5bae0acc51d0467ea809a87487fb9a5be6888a52db6d14563676c8ce8fa3c`  
		Last Modified: Tue, 04 Nov 2025 01:50:02 GMT  
		Size: 155.4 MB (155388117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a2291d082e640ce187f7c09d19695b942b2bbff7a670fd9392b7dcb86fb17b`  
		Last Modified: Tue, 04 Nov 2025 01:50:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:985fefaed90ae4275bd3498273d2b5bff0c68073ade0a24987505b210ac4337d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bedc4fa09680d44ab78532c8ec4c17c6164440a10ebf591a7960381debe3401`

```dockerfile
```

-	Layers:
	-	`sha256:c73dbdc04a315b11f8e04ac9f6d42e4a08def6925be0b71246bb36ccc0923bf2`  
		Last Modified: Tue, 04 Nov 2025 09:02:36 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27665359883bca78e432dfbaf04d6aad9ba8830c21d325b20d1fa9987e196944`  
		Last Modified: Tue, 04 Nov 2025 09:02:37 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e91781bb5c75b68df73f8dddcbe5d0b8bd7ab8886d556e9dd6a5bc57e249bf22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409148875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ce5fc2e06dcbdcd7d6447aa3f34194b771307373c175165d0ca7421ee6d3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7597b32b86f33d6cfe1536df796fc6ad77a63b0669d9f0f90ba38d5485891baa`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570728235470284f5444d9ae662ec0ae42d0fccc593389c9aba70d180166829`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198872149605ccef2bc20a708965178952a163fc95f8ed11419cc298c8b14cdb`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672c735e2472c8fa62a4f46f39518b8c0dffb6f261f1d9a1710ae08300e7ee9`  
		Last Modified: Fri, 24 Oct 2025 20:03:18 GMT  
		Size: 188.8 MB (188795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8001eb9d6f76ebb7d37099515e9ab0b040cbd0c46858de0a55ff98651a863`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:5e0bf498d04d76afae3343d9e9fc06cfc4e3ab0ad97e0f1d01cf65d8eac588be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766121325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e922d9ab00a0c2ad8f861df765bf0bce0e6afb5cd8e20d1494d600b708a4782`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:03 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:11:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:11:05 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:13:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49096beec96dd6d9b8b02ecc62cb846825eb45de97ab036485e13e3eb5d808fe`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6b457c4fbfcbdf61ab708c862ff837a7fc331fff6df5dac7075f5ce1be901`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d762a60280ee7c3798a5e61b737e41026a6f6cf3a47a1a612224ae52b9152`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a8f91cd7872519b244ce28b3ad3e5def0b9a34e53237536890d2a19d700060`  
		Last Modified: Fri, 24 Oct 2025 20:03:13 GMT  
		Size: 188.9 MB (188921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f795e174a6876adc6451536991eff371fc61e619c8a6395a0c4ca646df53`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-alpine`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.21`

```console
$ docker pull julia@sha256:d1a3e070ace2a47e5eb3cf2e507a090c9b0be78e986d61fa40b7b708e53a3842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.21` - linux; amd64

```console
$ docker pull julia@sha256:52ac97bc4b7d2863b731985c6614a46e6ab4f13f13f3c8d91d933a5c13055102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181941938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df008c40538a112568d8ff3054242fbabee9d18edd7f08445c7c38cf6f7cea4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514bda53ebb21b1322cf919f16ba5b28ae9b1d9acd8c0d0da1518623793417c9`  
		Last Modified: Sat, 11 Oct 2025 01:40:30 GMT  
		Size: 178.3 MB (178298998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d772ec346b861be7ae3ae4939fab2ea82732b66bf0931f5d9a7cb217646c0c6`  
		Last Modified: Wed, 08 Oct 2025 23:29:13 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.21` - unknown; unknown

```console
$ docker pull julia@sha256:9b1b7279a096a1493387b3ed071e6f6201a78ed8dfd3ecc09596e34b48a8e105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 KB (92841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a9169be517a413e716324eb64afaf1e70b5e4bf29b7ab8205696d41c42cfd`

```dockerfile
```

-	Layers:
	-	`sha256:d87cc8698e0b72551245a2ae783ddb2d064e0bf0c6a2b90e877668ed5777c209`  
		Last Modified: Thu, 09 Oct 2025 02:02:25 GMT  
		Size: 80.9 KB (80869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b3221cfc383c0844d2d950de60a17caa749b9d059d4a7e43848dc1f00be791`  
		Last Modified: Thu, 09 Oct 2025 02:02:26 GMT  
		Size: 12.0 KB (11972 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-alpine3.22`

```console
$ docker pull julia@sha256:98a1eb490414336864101b8c94a2e90ee254b1f28426d3d27e400667f247073c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `julia:1.10.10-alpine3.22` - linux; amd64

```console
$ docker pull julia@sha256:0a05cec5a5808854bf9e08020717f19ab220288352a10ba530b6c6c10bd4ca0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182101972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4336e8c37de4a095b7508eda269529106d2e7bdb08957beae9778ec4c5b2c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 30 Jun 2025 22:50:32 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["/bin/sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_PATH=/usr/local/julia
# Mon, 30 Jun 2025 22:50:32 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Mon, 30 Jun 2025 22:50:32 GMT
ENV JULIA_VERSION=1.10.10
# Mon, 30 Jun 2025 22:50:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			url='https://julialang-s3.julialang.org/bin/musl/x64/1.10/julia-1.10.10-musl-x86_64.tar.gz'; 			sha256='2d109f3f96f2be8ea45a0676f506642c20d972aeb3d526e8fa10ed49c0d6c786'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		wget -O julia.tar.gz.asc "$url.asc"; 	wget -O julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum -w -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apk del --no-network .fetch-deps; 		julia --version # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 30 Jun 2025 22:50:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 30 Jun 2025 22:50:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ea4970e4376faba0141c819e7e9841475cfd981d7e18d5cae797cbdf15bb07`  
		Last Modified: Wed, 08 Oct 2025 23:31:22 GMT  
		Size: 178.3 MB (178299153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920f924133a1281b577cc0acf2825c6808c96165b723d8b2ae75410db97d70e`  
		Last Modified: Wed, 08 Oct 2025 22:39:30 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-alpine3.22` - unknown; unknown

```console
$ docker pull julia@sha256:efeac4ecb897046a7df36968334d365c11453450588a8cf345295d37b7bffb42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 KB (94853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff0cded8704f83b2056ef09688dd480771f7a566b586093b6c4b0e9845c390d`

```dockerfile
```

-	Layers:
	-	`sha256:17140f826eda01d3eb3f979ce337e9721754f379052b630a846b103ab5059f1e`  
		Last Modified: Thu, 09 Oct 2025 02:02:20 GMT  
		Size: 82.3 KB (82264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec89d2bf69090ae637ecc3f91965ecfd58636ae6a78430faf934202d0213cd86`  
		Last Modified: Thu, 09 Oct 2025 02:02:21 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-bookworm`

```console
$ docker pull julia@sha256:45bc4dbc25e99e4b1627d875a0bda9ecaed7594eaf2e912063716b1362fda24e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.10-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:4bda83dd9a39110c47872fbd25d5057c3047dc8abb9d6b35a4ecfffdc8b658fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604899d2fa1050f182d1ae5bdd15c2139e2e41a41de28b1047db8ec9ab5ef848`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:18:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:18:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:18:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:18:51 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 00:18:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:18:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:18:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:18:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ace6d66d3a3d6fad5a1bd31565e9c119574e312dbf2c55d7ced0a4d992e9`  
		Last Modified: Tue, 04 Nov 2025 00:18:36 GMT  
		Size: 5.7 MB (5716426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da679be7402174d1185b0f17606b867b98643f73c7cc95dad0b2e16e00e91aa7`  
		Last Modified: Tue, 04 Nov 2025 09:17:33 GMT  
		Size: 176.3 MB (176324335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ec3b59508703ca5638df6b1d2ccb4ed5dfca4f8f5b3953902996e63a9752af`  
		Last Modified: Tue, 04 Nov 2025 00:19:27 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:40296d09536d5f80ac4ed2eccc4049db6cf1491bd847556f10ebd7f36116282c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a33f7225ff743e63ef62a204c797d11c5a29efdcb08c8965634d8d26976e27`

```dockerfile
```

-	Layers:
	-	`sha256:f4aef0138ce6bbc8ea4da422c1c364780680423a81a060249c4f7cb9bf45d403`  
		Last Modified: Tue, 04 Nov 2025 09:02:34 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0686819fa2a869291ce7e8dc1fcb09fae37060d173cd79a20b1de8844add2377`  
		Last Modified: Tue, 04 Nov 2025 09:02:34 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:1ec42c0c95b1341e44e12c2695533d415cd2be98d56220e9b4642e76a1df6f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c107bfdd9769f8548f754a55d66e3d432102dcdb9aa2974ef66a28c05a6bc6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:19:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:19:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:19:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:19:01 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 00:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:19:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:19:01 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7199a6c929b6d0910d53e32159d8d4a96b2bbfe63afacda8c1e08bb035462`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 5.6 MB (5567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611c49edecb508eb5b7510f801fee4729fcfb600b2b73b6db6be2f2f0365dab4`  
		Last Modified: Tue, 04 Nov 2025 00:19:34 GMT  
		Size: 177.4 MB (177412350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55bcc1527376498bd93e948c85f62591d0492f5bb15eeda78d20ab142059d63`  
		Last Modified: Tue, 04 Nov 2025 00:19:40 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:87a8730a90649d840d5f24ae412f951e490000dd220f1989fa1695182997034d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73ad65d708f63b3872a16d44e8c018aaf7edcec65ab54368c5c96c676f44319`

```dockerfile
```

-	Layers:
	-	`sha256:f569c5c87967337d10be32d568c5ac44fc56c4b88402a058bd81df78d420e4d0`  
		Last Modified: Tue, 04 Nov 2025 12:02:52 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5cab54a5a58f38337b3daee8c455212d5897c346f28d803bada61596cd8cbd5`  
		Last Modified: Tue, 04 Nov 2025 12:02:53 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:3f8a03007a027f5f20513ee68ebd0a4914c1a915322ae87a32a0a3e018b38cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd0a2d4c889e7762ae48f4c42cf198a6a38e1b63252ecb73f5efb24619edbb0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:36 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 00:16:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e53a671270cfb23b9ecd0c61dfb767438f7bd0aa02c20b42ced4ecbf32a253`  
		Last Modified: Tue, 04 Nov 2025 00:17:09 GMT  
		Size: 5.9 MB (5878028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e10bc4e2aeed2fb8b6386054cb6547de65c096b7bc6c6cb836c643d8d685a4`  
		Last Modified: Tue, 04 Nov 2025 00:17:03 GMT  
		Size: 157.8 MB (157807873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae666ec88791443865c71578b87e96283e5411ccd94556d767edd2c310e1929f`  
		Last Modified: Tue, 04 Nov 2025 00:17:08 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9911c0cf4f0835c4a0c063bb70e1140e14346b1a06f8675631dce10b3dc28c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd660a1b3cd0cc5ff60569943183acbdce5ca4c6a731ccfb6c4f5ee20f28035d`

```dockerfile
```

-	Layers:
	-	`sha256:3d673b10015287f5de9c3c019a35ec5369e0c1b68fa12329a2344b62f3c59a70`  
		Last Modified: Tue, 04 Nov 2025 12:02:57 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:918cb1649ded3944e7056193f9e0bda5bbd02a3d20b2558fea3a1d963c55689c`  
		Last Modified: Tue, 04 Nov 2025 12:02:58 GMT  
		Size: 16.6 KB (16573 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:49ad9e9a851899eae8db8a17307e95d55cc252ca3115e708e6c22cf5d16f29eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6492624703a3f7d8b9062f3f6cf47e9b81088f95b8e653693f283a5627c5dfc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:51:01 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:51:01 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:51:01 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:51:01 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:51:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:51:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:51:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:51:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100319a5fe2f62c408488b2652211045c6a4b819d76492b9ffce2f37abb9ba00`  
		Last Modified: Tue, 04 Nov 2025 01:48:02 GMT  
		Size: 6.3 MB (6256339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3923a442c8b8de51892aacbd2e260437a31b5d25e44fa1272bc7b7d882050235`  
		Last Modified: Tue, 04 Nov 2025 01:52:00 GMT  
		Size: 155.4 MB (155354872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f666d81055dddc17b4e4dea946788cea14b6835875e87b6ee934c072f207841`  
		Last Modified: Tue, 04 Nov 2025 01:52:06 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:baa9c4c07f62fe7eadc751e107b67d8e0371c7a99682f9228f71f9d82edd9e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0275c7ea898dc2ec596c40d092455f811b73c995e90fed1e5fc9efa4f7e541`

```dockerfile
```

-	Layers:
	-	`sha256:3e2bbb0dea0422671dfbd677f0bdf76d17779b3f4339d0ca0637092f34f335c6`  
		Last Modified: Tue, 04 Nov 2025 09:02:45 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5312dfccac519202c283edee182da0b928b65aba35e434e5bf49819d90593fd8`  
		Last Modified: Tue, 04 Nov 2025 09:02:45 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-trixie`

```console
$ docker pull julia@sha256:6e8a24f3468fa547cd15dd2a570b18083fc3e34b70bfc02f220aedf8c5064df6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.10.10-trixie` - linux; amd64

```console
$ docker pull julia@sha256:0be1836fe29b84a81a3f2392499be0f1f19c4aaba202b4503236a853d2c0bdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212383412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7241add4df9b1f679f3bba4863c0fd58aa7e854b0c5c191b90755d1730539cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:06:14 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:06:14 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 04:06:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:06:14 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d74ee65a5c8887d4e897ad989f11f0bcb62ac7d2366e03e4d3ed724098c6f9`  
		Last Modified: Tue, 04 Nov 2025 04:06:50 GMT  
		Size: 6.2 MB (6242791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bd14cb66cc421efef6c3fc4e502fd4f14ed34b531bfa9b946175248f8d1457`  
		Last Modified: Tue, 04 Nov 2025 09:29:48 GMT  
		Size: 176.4 MB (176362146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d063ea66e0ed144e5d9961751f21aa086e38f006ed44b8ffc92457cb43d3f4`  
		Last Modified: Tue, 04 Nov 2025 04:06:49 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1c90a143de00756516f02bf7f4ad670b4a85d2ef7b78eacf9929d6f8658c5b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578816bd108370e2ee32c28f6037aa88efa133e3c9f498b49e73a2de57e96728`

```dockerfile
```

-	Layers:
	-	`sha256:783cad2d993fc11df084756d4ccf86ec7a818d3b9f352da4e1acb6bbf8be3284`  
		Last Modified: Tue, 04 Nov 2025 09:02:24 GMT  
		Size: 2.2 MB (2240153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3ab0badf666ea173f8c9198febcc7bf3be71d34dffca9fa4ebc6d5e1dda07ce`  
		Last Modified: Tue, 04 Nov 2025 09:02:25 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9034543a863fa5fc83a8c69b7184f76407be8c11175f7755e8c62999622bf30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213746025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5054084ef14e78af405d41a58123fa0216271b8d270ac19eb938e6582e7c64fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:05 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:05 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860a1cc05c2a5182c3ec611330be4e7f8a4c3614cd9c6fc64939f840fe39b922`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 6.2 MB (6153088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd484f8a8c3f57b03b0dde9fbb6287c235f5c2653c66d13c4633d32e4e0169a3`  
		Last Modified: Tue, 04 Nov 2025 01:20:39 GMT  
		Size: 177.5 MB (177450266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d256230749ee4d70eb88e530866c8bf1253a3357a5aa6011e17147806ad8a9d`  
		Last Modified: Tue, 04 Nov 2025 01:20:45 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:0cdd53a235d899ab26f0c20cabbf1efe2cc48c674192f8bafbee32df5f667201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ef3c90a2821939161b2950600b3d5816b697f05e1532322ee2578c4f52c76d`

```dockerfile
```

-	Layers:
	-	`sha256:c4398e34af44927e8155eafa68eb073a99ed6cfa72d627792f13955a0957e572`  
		Last Modified: Tue, 04 Nov 2025 12:02:43 GMT  
		Size: 2.2 MB (2239203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffdeb45a064847163ddeb413336129bf867d70ca72df0a108051a8038638d2b5`  
		Last Modified: Tue, 04 Nov 2025 12:02:44 GMT  
		Size: 17.3 KB (17286 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:e423563d8d90d8de959bc69db5b809d77585d80edc7ac937d43931c64bab6608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195564686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ffdd11d10ae385984d8501a7a11622fd3265ac316188a775ecfb5d6dc85f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:02 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9aeb3401bd2d24090ebce607bb50fbc32e48f39c0a9293e5a98af40be3141`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 6.4 MB (6427758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b334668a8683483982a48e9af66fe679c9746cd98e0a3588db6b5f9e5cfd779`  
		Last Modified: Tue, 04 Nov 2025 01:20:27 GMT  
		Size: 157.8 MB (157841776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc6d0c4617c43fd875c9e587f50ae36b4ffb5519cae63ed329bf009cdeae2c3`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2891e0bd4ec4a6f4294f4c88edee7cf05ecfc3ebb3c188c6889d4ac6fb5ba8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3f0e4f385ef87fcf0c92eda1160d601a585513182bc8df78ac4f731cb2c44`

```dockerfile
```

-	Layers:
	-	`sha256:11bd16cd6a5af46bf23b9e389a3da58347e894fd75ac31bd79639b6ddca2e8b0`  
		Last Modified: Tue, 04 Nov 2025 12:02:47 GMT  
		Size: 2.2 MB (2237298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7a63328180c5d7a2e69d92179f82b64dbcf17de8dcf8c719d2b4cebb2a400b7`  
		Last Modified: Tue, 04 Nov 2025 12:02:48 GMT  
		Size: 17.1 KB (17134 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:34d9137560b8a388693b28f459d724687334b78f8870877694eb3c169ce669ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195669346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef672dde653052764643aaaf988bd53503470b382112a62899b3b2acbe462f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:49:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:49:03 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 04 Nov 2025 01:49:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:49:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:49:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b5bae0acc51d0467ea809a87487fb9a5be6888a52db6d14563676c8ce8fa3c`  
		Last Modified: Tue, 04 Nov 2025 01:50:02 GMT  
		Size: 155.4 MB (155388117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a2291d082e640ce187f7c09d19695b942b2bbff7a670fd9392b7dcb86fb17b`  
		Last Modified: Tue, 04 Nov 2025 01:50:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:985fefaed90ae4275bd3498273d2b5bff0c68073ade0a24987505b210ac4337d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bedc4fa09680d44ab78532c8ec4c17c6164440a10ebf591a7960381debe3401`

```dockerfile
```

-	Layers:
	-	`sha256:c73dbdc04a315b11f8e04ac9f6d42e4a08def6925be0b71246bb36ccc0923bf2`  
		Last Modified: Tue, 04 Nov 2025 09:02:36 GMT  
		Size: 2.2 MB (2242648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27665359883bca78e432dfbaf04d6aad9ba8830c21d325b20d1fa9987e196944`  
		Last Modified: Tue, 04 Nov 2025 09:02:37 GMT  
		Size: 17.2 KB (17213 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-windowsservercore`

```console
$ docker pull julia@sha256:1621a74d40ee0b36a332a7f33bcefbb97c824db63e656ae6d7404fe653846166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.10.10-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e91781bb5c75b68df73f8dddcbe5d0b8bd7ab8886d556e9dd6a5bc57e249bf22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409148875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ce5fc2e06dcbdcd7d6447aa3f34194b771307373c175165d0ca7421ee6d3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7597b32b86f33d6cfe1536df796fc6ad77a63b0669d9f0f90ba38d5485891baa`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570728235470284f5444d9ae662ec0ae42d0fccc593389c9aba70d180166829`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198872149605ccef2bc20a708965178952a163fc95f8ed11419cc298c8b14cdb`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672c735e2472c8fa62a4f46f39518b8c0dffb6f261f1d9a1710ae08300e7ee9`  
		Last Modified: Fri, 24 Oct 2025 20:03:18 GMT  
		Size: 188.8 MB (188795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8001eb9d6f76ebb7d37099515e9ab0b040cbd0c46858de0a55ff98651a863`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:5e0bf498d04d76afae3343d9e9fc06cfc4e3ab0ad97e0f1d01cf65d8eac588be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766121325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e922d9ab00a0c2ad8f861df765bf0bce0e6afb5cd8e20d1494d600b708a4782`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:03 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:11:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:11:05 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:13:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49096beec96dd6d9b8b02ecc62cb846825eb45de97ab036485e13e3eb5d808fe`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6b457c4fbfcbdf61ab708c862ff837a7fc331fff6df5dac7075f5ce1be901`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d762a60280ee7c3798a5e61b737e41026a6f6cf3a47a1a612224ae52b9152`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a8f91cd7872519b244ce28b3ad3e5def0b9a34e53237536890d2a19d700060`  
		Last Modified: Fri, 24 Oct 2025 20:03:13 GMT  
		Size: 188.9 MB (188921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f795e174a6876adc6451536991eff371fc61e619c8a6395a0c4ca646df53`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:9c6803f12356d3db735091ee7ac10cf1948f49c1ab0c3211cd81833d520f9936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1.10.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:5e0bf498d04d76afae3343d9e9fc06cfc4e3ab0ad97e0f1d01cf65d8eac588be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1766121325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e922d9ab00a0c2ad8f861df765bf0bce0e6afb5cd8e20d1494d600b708a4782`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:11:03 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:11:04 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:11:05 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:13:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:13:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e52f723ea76815eba0509acf58234aca0dcfb87d86550ea2dcb0731023df7`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49096beec96dd6d9b8b02ecc62cb846825eb45de97ab036485e13e3eb5d808fe`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e6b457c4fbfcbdf61ab708c862ff837a7fc331fff6df5dac7075f5ce1be901`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d762a60280ee7c3798a5e61b737e41026a6f6cf3a47a1a612224ae52b9152`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a8f91cd7872519b244ce28b3ad3e5def0b9a34e53237536890d2a19d700060`  
		Last Modified: Fri, 24 Oct 2025 20:03:13 GMT  
		Size: 188.9 MB (188921845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b536f795e174a6876adc6451536991eff371fc61e619c8a6395a0c4ca646df53`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:6150fe17c6457736dcfafe2d184e7f5f9bea7e44d25de1573bbbbdeb511c1f68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1.10.10-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e91781bb5c75b68df73f8dddcbe5d0b8bd7ab8886d556e9dd6a5bc57e249bf22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3409148875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f44ce5fc2e06dcbdcd7d6447aa3f34194b771307373c175165d0ca7421ee6d3`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_VERSION=1.10.10
# Fri, 24 Oct 2025 18:13:06 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Fri, 24 Oct 2025 18:14:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:09 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7597b32b86f33d6cfe1536df796fc6ad77a63b0669d9f0f90ba38d5485891baa`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d570728235470284f5444d9ae662ec0ae42d0fccc593389c9aba70d180166829`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198872149605ccef2bc20a708965178952a163fc95f8ed11419cc298c8b14cdb`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672c735e2472c8fa62a4f46f39518b8c0dffb6f261f1d9a1710ae08300e7ee9`  
		Last Modified: Fri, 24 Oct 2025 20:03:18 GMT  
		Size: 188.8 MB (188795251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e8001eb9d6f76ebb7d37099515e9ab0b040cbd0c46858de0a55ff98651a863`  
		Last Modified: Fri, 24 Oct 2025 18:23:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:72d31648b71496d1e53aaf82c36e92f7aac487bc633811d4c9af223f80937ab9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:6221aee6839236bb4d2252758931755a84fb7b6fa47c3b194ea4c51585f03fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b57b9e4ac3820f22f9e8cceb5f60d41ed4a3081fa08a9aa610c5fac0ff447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 04:05:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408e36a7e1d73b96137de5bd71a78afb2ce588d6cd94b57dae5b78ad9d4948`  
		Last Modified: Tue, 04 Nov 2025 04:06:34 GMT  
		Size: 6.2 MB (6242838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e6cdd48a9666f4057b7a1006373d8006398052be9cbb55b7d8d95ec461a66`  
		Last Modified: Tue, 04 Nov 2025 09:10:51 GMT  
		Size: 288.8 MB (288825525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96191142a13dce96425c47257e8e0733fe4729b8733b5989dca96384458c843e`  
		Last Modified: Tue, 04 Nov 2025 04:06:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:8ff24e1f58421f64c451467350f044c2cdec90316bab6588d98e10446143e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424ed2184a8bbaf12f7a112609faaa2208b5bbabafdbf269835ddb96c218646`

```dockerfile
```

-	Layers:
	-	`sha256:41ce5b3eb055a8dd7cc5be314e1f5f0ec46e20e5886d253771f76b579abb3711`  
		Last Modified: Tue, 04 Nov 2025 09:02:55 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142507089fe0778974555b71bc47ec0a3c0dec3255adf7bfe9cb83cae1fd61ae`  
		Last Modified: Tue, 04 Nov 2025 09:02:56 GMT  
		Size: 17.2 KB (17151 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd0a2471c77bc81d4b77c7279d9982dd87d4a92d65cf2f4865f3bb3e469d62f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f325fd60152ce42b1e02f5021518978f1fe205a1745a217d479b5f65059f37a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a17ece07a394ffce3a2ea1e4714b628c8bf0d7c1629223d158c65c3990d10c`  
		Last Modified: Tue, 04 Nov 2025 01:20:29 GMT  
		Size: 6.2 MB (6153077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bac822b894e42e6cb67af04484131a8b4bc33e7e87591e151a35df4de147`  
		Last Modified: Tue, 04 Nov 2025 01:20:22 GMT  
		Size: 304.7 MB (304672762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86be4a1a181e230e85c044a97f7b710551e6d3bf203afc1479aa8dec343df8c5`  
		Last Modified: Tue, 04 Nov 2025 01:20:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:3c7d0ddde8cb352b70fbdda3a78f3771649ae2c9f239e1e087a2daf3d1323e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bed5c4f013812b64b7b7548c810216a9414373d254e64202f69f68d1d0a727`

```dockerfile
```

-	Layers:
	-	`sha256:dfb9bdbb320e3971cda2c08a579290fd64f4f60838c198d9965b3894cc1fd437`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651226e0dd9d108de2bd4156ffe234f9d2c9ca527fae2c31797ab0d56e9bd622`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:d0b9d84847198bf7fa4453e2efe114db22eece072ba127bd4bdad755b21ab5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0b9670cd872909a31e44da8896181024f3a6554924009bcbb1d2141b18ee13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c4b44632242d439bd005ebb4d6616cd3a08772d224b9b7502af79bdf4b68`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 6.4 MB (6427799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1daf36fab91b2c580863fb421e918de2ded562304042a54df48addeffd07e1`  
		Last Modified: Tue, 04 Nov 2025 01:20:37 GMT  
		Size: 237.6 MB (237589306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26e42ea4da86b177c44034edbaee4d859f9d0ab93359709663e5b17845d431`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:ad35efca310a83724a463f62361641c237dfd0378d58193f57b4fd3549454149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968db347a32b2121fad86e5bb44a227a1fd3fbaa351e2f0b4dd37bf7a8fe2001`

```dockerfile
```

-	Layers:
	-	`sha256:3fd63a11e5039d0d9fd4fc07a7da6491e5279e6aaa6374d76d917440d26cffc2`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf1b6e8427f90711ea68122baffe32232ee2406c2d466e6bd28623f5ce8e6fb`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; ppc64le

```console
$ docker pull julia@sha256:af47fb9d083edb11b690b7a11bad7359b5a825e53e17355ce33e5e36aeb1723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd7daae7a851023d0e7ba4bfcb25275c9cf4e771c4b29c79cc666f417b2c309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:43:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804e3fa9e2b6d927adbfa2f484f29c48dfa02fa48ae6053634015859c5e44bd6`  
		Last Modified: Tue, 04 Nov 2025 01:45:10 GMT  
		Size: 248.6 MB (248575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59577986c334ac00b0537217cf3e085fba567d1ca11371d7d1f6e6e51bcc01`  
		Last Modified: Tue, 04 Nov 2025 01:45:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:8d43151df46a2c7140ba113af82ac260984f5cdafa2d1aa3dd9a7a2d321c207a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5817953051e2c01f0b487428d6642914ca32726c040f3030dfd8d467629ae7`

```dockerfile
```

-	Layers:
	-	`sha256:e9ea77425e0dd2f93981c3f6e5a450d1db4f1dc4572401f3b7964e76845874f7`  
		Last Modified: Tue, 04 Nov 2025 09:03:05 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7a3c3343500104211cda157133385e0318084ee640711be6d3e6a8ed21690e`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:3e4b6f02eb3db1f6f7fef665b79b647bd37482922c5bd8a39fc708700f6fe84e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49ef7f991db05bb94358171660b480fc0d722a820dca21a283c76a99f9c7204`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:13:08 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf1bb93f61e8c24fd4e2b3d6e7c1a7943daee471638a5102faccf0d22074f09`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d22a566df8f51c2575151699d1be7aded51355ae1069d6af81823f790845c7`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d376dc10fa6d5e6059e0f1c0458cf2f4a223cc933933219de01bc9d41f882c`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988b521dc749bef6ad5f6bd2bb5db65fb89261ab2f61aafad478ae081e56571`  
		Last Modified: Fri, 24 Oct 2025 20:03:28 GMT  
		Size: 286.0 MB (286040248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f857510290685f39eba099823626c8691f0e82156ca14232c875a5d04cee0cc6`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:3fd4821b551758c3327c024812ef254c02fccf931c0f149e703ef745a873d9e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863360535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c1c7e41c981d2d881f5280ed35b21cb891d6df13f80c5dbadd26a513273967`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b16e8884054f88f5b487e2736f79d2954386da590bb81cb5d157d5a32f0f6a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc97c885b2f12dc27a3f7692682304abf5cec4dca32d7105ed1e2c395c460f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e6a67941039a29b42f6001a5508703e7c5c84c75be187b38ca35f648d1768`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573a7892a8d07b89b24a2cb6ac382cb5e310149f59ad0bb2009ccc4cb665f2a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d057c66fb4ace98f74ecd96c641e284c587bd5071339e8c0b47e5e91713a76`  
		Last Modified: Fri, 24 Oct 2025 20:04:02 GMT  
		Size: 286.2 MB (286161015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bfd8c3a8e1bf28c28bcf735b62a68e683820c2450b6278ee68fab3bd28440`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:2634749aa561c40e9ccc10bce1d63a2623ef932d6f6bd74e33eee9b02dbc1df9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:a2fe0230f127a23f688122ffde0dd7328c55ac5abdc12b360a1118f4a4f9809b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f3018decd8c10a81d1829ebb3c9ba98903a27aef46a930508307a2b963dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:18:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:18:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:18:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:18:58 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 00:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:18:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:18:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0dfad91cddb56b269dd4265bff9adb9b968d1c56c89241fe585d73572306d2`  
		Last Modified: Tue, 04 Nov 2025 00:19:50 GMT  
		Size: 5.7 MB (5716353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ef9c9497633959219112e8f0da9221b46d7fa94def22e71ab58e4de924b039`  
		Last Modified: Tue, 04 Nov 2025 10:56:24 GMT  
		Size: 288.8 MB (288788397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bf51bf4728bf1dbae8d828dfa99fdab9ef0f956e4af2e4843dfacadc6f993b`  
		Last Modified: Tue, 04 Nov 2025 00:19:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c00fc06fe8ac263b8606cbb9a83e61eaf38b57c2913a727db8ed42bbc87a8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c5d4f537d6162002130dc9ef35297e503974412f8938b29ea34e28d17cc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:932f9013aa1207eb422105ff1dc02fee44727414af05f7e2c9a70b2cb63c06c8`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f49e1730c5fb92267f29b860f3442112ce35e8e3a1f28c2f6738fcb89bc9cce`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2a8bede234d41d0f94259d2351d4c4568d0d3716c47711ef37ceaf917b0838e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5c71b8f02318901391800db522c443b104a331183a997a5f256157d6d7d4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:19:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:19:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 00:19:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:19:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd30e2e96bd67e71de351f0a116cd53aec6bf644d0116f902fc59868bba065`  
		Last Modified: Tue, 04 Nov 2025 00:20:18 GMT  
		Size: 5.6 MB (5567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c037fffe78b941f610f3b4982b1f837f57f07a2d8b2902b51b7c90f67b2418`  
		Last Modified: Tue, 04 Nov 2025 00:20:08 GMT  
		Size: 304.6 MB (304646620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d07b723d472689e559c347328896264c36f5e1ec6d927e17fbc954cebbfdc`  
		Last Modified: Tue, 04 Nov 2025 00:20:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:611d957b656a75d051f322ce53e6e21cd2a951bc4ad320a533b0dbb650eaa35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee19cf5f710dca293dab6d0e2310873aae6dccc6702258b16a8854a1a4d65c2e`

```dockerfile
```

-	Layers:
	-	`sha256:2b84519d466535234c7b5055d976677cbbc9eae041c214964088acbf1de2eade`  
		Last Modified: Tue, 04 Nov 2025 12:03:22 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e86b6e2662fd1b1299cdb8b36344b6c0fce8718e112fb2deabaefdce3624a7c`  
		Last Modified: Tue, 04 Nov 2025 12:03:25 GMT  
		Size: 16.7 KB (16678 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:ad1f215325548359ca1f57fda6ba0cd638621f8b28ab318f6b1ab3196011eeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272644005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6563ff2d41e29147321dfa66b88666c62a23c210c8853ffce3a19bd4495c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:44 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:44 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:44 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:44 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 00:16:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d04fdc9b583a90fae6ec25b6bb90ea916644cd2a3c783251d14bbaa59db246`  
		Last Modified: Tue, 04 Nov 2025 00:17:50 GMT  
		Size: 5.9 MB (5878043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c917cc869a978d2e1cdac0e3c181898c15669a9358dbc98875f13aae34dce00e`  
		Last Modified: Tue, 04 Nov 2025 00:17:24 GMT  
		Size: 237.6 MB (237555746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c3466306423d1e76b5f8cc0bff2a744960f44b64597382de8df3572fe46c12`  
		Last Modified: Tue, 04 Nov 2025 00:17:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5be748747d7a159189e996d25f19ba3ad772900a1bc32e7a40377f9088d3cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3d49d001f84f5006065b8107684fd28eb43a9d54c3af38c74473af0b90126`

```dockerfile
```

-	Layers:
	-	`sha256:fa4523ff217295caccc18459923699b70721b17c199ad7371860c7e532616883`  
		Last Modified: Tue, 04 Nov 2025 12:03:28 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae0f1a4a0fa0f1549b411797551910075f2ab2fb076166ed67a841318b04d0c`  
		Last Modified: Tue, 04 Nov 2025 12:03:29 GMT  
		Size: 16.6 KB (16559 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:ee59c2dff4a5dbbab3fb3f333fec5887c9b9d7233d98ef628b0cec97d378d000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6f6bfa81dc86a6798fb3f5015ccf4c0ff7ca6661362ab341452e571c31161f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:46:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:46:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:46:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:46:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:46:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:46:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100319a5fe2f62c408488b2652211045c6a4b819d76492b9ffce2f37abb9ba00`  
		Last Modified: Tue, 04 Nov 2025 01:48:02 GMT  
		Size: 6.3 MB (6256339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e673a344de582bf81f4cf828559313cbaa253124528d26c65c9e56283c0d00c7`  
		Last Modified: Tue, 04 Nov 2025 01:47:55 GMT  
		Size: 248.6 MB (248553781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5facd3c79b38c0ef21d97c2a0005bc5d07496e0c3b714da014de64d7af279ea8`  
		Last Modified: Tue, 04 Nov 2025 01:48:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f0dce5c9ddc2c4debdb683133976ae30975dd94a706e69821de44d55d8603595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2855d2c1f1953b5fae2e9fa8202910f64f0dce318728d0b94a42167874116c`

```dockerfile
```

-	Layers:
	-	`sha256:8322998454ca23430e1103826490dffb82114bbd02ded45435ee184f05ad8630`  
		Last Modified: Tue, 04 Nov 2025 09:03:16 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8a94bdd45295600accfc923ee1509e5ae779d21db84deb8c2546eaf2fd1db2`  
		Last Modified: Tue, 04 Nov 2025 09:03:17 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-trixie`

```console
$ docker pull julia@sha256:0bb482133691815f3c5f7da53758f9e12902f713286382b17ac4e41d1e04f018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11-trixie` - linux; amd64

```console
$ docker pull julia@sha256:6221aee6839236bb4d2252758931755a84fb7b6fa47c3b194ea4c51585f03fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b57b9e4ac3820f22f9e8cceb5f60d41ed4a3081fa08a9aa610c5fac0ff447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 04:05:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408e36a7e1d73b96137de5bd71a78afb2ce588d6cd94b57dae5b78ad9d4948`  
		Last Modified: Tue, 04 Nov 2025 04:06:34 GMT  
		Size: 6.2 MB (6242838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e6cdd48a9666f4057b7a1006373d8006398052be9cbb55b7d8d95ec461a66`  
		Last Modified: Tue, 04 Nov 2025 09:10:51 GMT  
		Size: 288.8 MB (288825525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96191142a13dce96425c47257e8e0733fe4729b8733b5989dca96384458c843e`  
		Last Modified: Tue, 04 Nov 2025 04:06:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:8ff24e1f58421f64c451467350f044c2cdec90316bab6588d98e10446143e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424ed2184a8bbaf12f7a112609faaa2208b5bbabafdbf269835ddb96c218646`

```dockerfile
```

-	Layers:
	-	`sha256:41ce5b3eb055a8dd7cc5be314e1f5f0ec46e20e5886d253771f76b579abb3711`  
		Last Modified: Tue, 04 Nov 2025 09:02:55 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142507089fe0778974555b71bc47ec0a3c0dec3255adf7bfe9cb83cae1fd61ae`  
		Last Modified: Tue, 04 Nov 2025 09:02:56 GMT  
		Size: 17.2 KB (17151 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd0a2471c77bc81d4b77c7279d9982dd87d4a92d65cf2f4865f3bb3e469d62f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f325fd60152ce42b1e02f5021518978f1fe205a1745a217d479b5f65059f37a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a17ece07a394ffce3a2ea1e4714b628c8bf0d7c1629223d158c65c3990d10c`  
		Last Modified: Tue, 04 Nov 2025 01:20:29 GMT  
		Size: 6.2 MB (6153077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bac822b894e42e6cb67af04484131a8b4bc33e7e87591e151a35df4de147`  
		Last Modified: Tue, 04 Nov 2025 01:20:22 GMT  
		Size: 304.7 MB (304672762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86be4a1a181e230e85c044a97f7b710551e6d3bf203afc1479aa8dec343df8c5`  
		Last Modified: Tue, 04 Nov 2025 01:20:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:3c7d0ddde8cb352b70fbdda3a78f3771649ae2c9f239e1e087a2daf3d1323e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bed5c4f013812b64b7b7548c810216a9414373d254e64202f69f68d1d0a727`

```dockerfile
```

-	Layers:
	-	`sha256:dfb9bdbb320e3971cda2c08a579290fd64f4f60838c198d9965b3894cc1fd437`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651226e0dd9d108de2bd4156ffe234f9d2c9ca527fae2c31797ab0d56e9bd622`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; 386

```console
$ docker pull julia@sha256:d0b9d84847198bf7fa4453e2efe114db22eece072ba127bd4bdad755b21ab5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0b9670cd872909a31e44da8896181024f3a6554924009bcbb1d2141b18ee13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c4b44632242d439bd005ebb4d6616cd3a08772d224b9b7502af79bdf4b68`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 6.4 MB (6427799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1daf36fab91b2c580863fb421e918de2ded562304042a54df48addeffd07e1`  
		Last Modified: Tue, 04 Nov 2025 01:20:37 GMT  
		Size: 237.6 MB (237589306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26e42ea4da86b177c44034edbaee4d859f9d0ab93359709663e5b17845d431`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ad35efca310a83724a463f62361641c237dfd0378d58193f57b4fd3549454149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968db347a32b2121fad86e5bb44a227a1fd3fbaa351e2f0b4dd37bf7a8fe2001`

```dockerfile
```

-	Layers:
	-	`sha256:3fd63a11e5039d0d9fd4fc07a7da6491e5279e6aaa6374d76d917440d26cffc2`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf1b6e8427f90711ea68122baffe32232ee2406c2d466e6bd28623f5ce8e6fb`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:af47fb9d083edb11b690b7a11bad7359b5a825e53e17355ce33e5e36aeb1723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd7daae7a851023d0e7ba4bfcb25275c9cf4e771c4b29c79cc666f417b2c309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:43:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804e3fa9e2b6d927adbfa2f484f29c48dfa02fa48ae6053634015859c5e44bd6`  
		Last Modified: Tue, 04 Nov 2025 01:45:10 GMT  
		Size: 248.6 MB (248575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59577986c334ac00b0537217cf3e085fba567d1ca11371d7d1f6e6e51bcc01`  
		Last Modified: Tue, 04 Nov 2025 01:45:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:8d43151df46a2c7140ba113af82ac260984f5cdafa2d1aa3dd9a7a2d321c207a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5817953051e2c01f0b487428d6642914ca32726c040f3030dfd8d467629ae7`

```dockerfile
```

-	Layers:
	-	`sha256:e9ea77425e0dd2f93981c3f6e5a450d1db4f1dc4572401f3b7964e76845874f7`  
		Last Modified: Tue, 04 Nov 2025 09:03:05 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7a3c3343500104211cda157133385e0318084ee640711be6d3e6a8ed21690e`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-windowsservercore`

```console
$ docker pull julia@sha256:7583e7051f75688be7143960b83180a73b4d1433393614307e9fbd7e3eac56c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:3e4b6f02eb3db1f6f7fef665b79b647bd37482922c5bd8a39fc708700f6fe84e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49ef7f991db05bb94358171660b480fc0d722a820dca21a283c76a99f9c7204`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:13:08 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf1bb93f61e8c24fd4e2b3d6e7c1a7943daee471638a5102faccf0d22074f09`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d22a566df8f51c2575151699d1be7aded51355ae1069d6af81823f790845c7`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d376dc10fa6d5e6059e0f1c0458cf2f4a223cc933933219de01bc9d41f882c`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988b521dc749bef6ad5f6bd2bb5db65fb89261ab2f61aafad478ae081e56571`  
		Last Modified: Fri, 24 Oct 2025 20:03:28 GMT  
		Size: 286.0 MB (286040248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f857510290685f39eba099823626c8691f0e82156ca14232c875a5d04cee0cc6`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:3fd4821b551758c3327c024812ef254c02fccf931c0f149e703ef745a873d9e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863360535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c1c7e41c981d2d881f5280ed35b21cb891d6df13f80c5dbadd26a513273967`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b16e8884054f88f5b487e2736f79d2954386da590bb81cb5d157d5a32f0f6a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc97c885b2f12dc27a3f7692682304abf5cec4dca32d7105ed1e2c395c460f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e6a67941039a29b42f6001a5508703e7c5c84c75be187b38ca35f648d1768`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573a7892a8d07b89b24a2cb6ac382cb5e310149f59ad0bb2009ccc4cb665f2a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d057c66fb4ace98f74ecd96c641e284c587bd5071339e8c0b47e5e91713a76`  
		Last Modified: Fri, 24 Oct 2025 20:04:02 GMT  
		Size: 286.2 MB (286161015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bfd8c3a8e1bf28c28bcf735b62a68e683820c2450b6278ee68fab3bd28440`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:3a20f9c4936f8e6603f2dd59188d3bdc3e043b9758a946b77fdaca90c6d18e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:3fd4821b551758c3327c024812ef254c02fccf931c0f149e703ef745a873d9e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863360535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c1c7e41c981d2d881f5280ed35b21cb891d6df13f80c5dbadd26a513273967`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b16e8884054f88f5b487e2736f79d2954386da590bb81cb5d157d5a32f0f6a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc97c885b2f12dc27a3f7692682304abf5cec4dca32d7105ed1e2c395c460f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e6a67941039a29b42f6001a5508703e7c5c84c75be187b38ca35f648d1768`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573a7892a8d07b89b24a2cb6ac382cb5e310149f59ad0bb2009ccc4cb665f2a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d057c66fb4ace98f74ecd96c641e284c587bd5071339e8c0b47e5e91713a76`  
		Last Modified: Fri, 24 Oct 2025 20:04:02 GMT  
		Size: 286.2 MB (286161015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bfd8c3a8e1bf28c28bcf735b62a68e683820c2450b6278ee68fab3bd28440`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:1d13bb74b64576b845b13bb0cd9f284ed2927b75732a5fcece2160c97100cd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:3e4b6f02eb3db1f6f7fef665b79b647bd37482922c5bd8a39fc708700f6fe84e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49ef7f991db05bb94358171660b480fc0d722a820dca21a283c76a99f9c7204`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:13:08 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf1bb93f61e8c24fd4e2b3d6e7c1a7943daee471638a5102faccf0d22074f09`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d22a566df8f51c2575151699d1be7aded51355ae1069d6af81823f790845c7`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d376dc10fa6d5e6059e0f1c0458cf2f4a223cc933933219de01bc9d41f882c`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988b521dc749bef6ad5f6bd2bb5db65fb89261ab2f61aafad478ae081e56571`  
		Last Modified: Fri, 24 Oct 2025 20:03:28 GMT  
		Size: 286.0 MB (286040248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f857510290685f39eba099823626c8691f0e82156ca14232c875a5d04cee0cc6`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7`

```console
$ docker pull julia@sha256:72d31648b71496d1e53aaf82c36e92f7aac487bc633811d4c9af223f80937ab9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.11.7` - linux; amd64

```console
$ docker pull julia@sha256:6221aee6839236bb4d2252758931755a84fb7b6fa47c3b194ea4c51585f03fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b57b9e4ac3820f22f9e8cceb5f60d41ed4a3081fa08a9aa610c5fac0ff447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 04:05:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408e36a7e1d73b96137de5bd71a78afb2ce588d6cd94b57dae5b78ad9d4948`  
		Last Modified: Tue, 04 Nov 2025 04:06:34 GMT  
		Size: 6.2 MB (6242838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e6cdd48a9666f4057b7a1006373d8006398052be9cbb55b7d8d95ec461a66`  
		Last Modified: Tue, 04 Nov 2025 09:10:51 GMT  
		Size: 288.8 MB (288825525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96191142a13dce96425c47257e8e0733fe4729b8733b5989dca96384458c843e`  
		Last Modified: Tue, 04 Nov 2025 04:06:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:8ff24e1f58421f64c451467350f044c2cdec90316bab6588d98e10446143e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424ed2184a8bbaf12f7a112609faaa2208b5bbabafdbf269835ddb96c218646`

```dockerfile
```

-	Layers:
	-	`sha256:41ce5b3eb055a8dd7cc5be314e1f5f0ec46e20e5886d253771f76b579abb3711`  
		Last Modified: Tue, 04 Nov 2025 09:02:55 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142507089fe0778974555b71bc47ec0a3c0dec3255adf7bfe9cb83cae1fd61ae`  
		Last Modified: Tue, 04 Nov 2025 09:02:56 GMT  
		Size: 17.2 KB (17151 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd0a2471c77bc81d4b77c7279d9982dd87d4a92d65cf2f4865f3bb3e469d62f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f325fd60152ce42b1e02f5021518978f1fe205a1745a217d479b5f65059f37a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a17ece07a394ffce3a2ea1e4714b628c8bf0d7c1629223d158c65c3990d10c`  
		Last Modified: Tue, 04 Nov 2025 01:20:29 GMT  
		Size: 6.2 MB (6153077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bac822b894e42e6cb67af04484131a8b4bc33e7e87591e151a35df4de147`  
		Last Modified: Tue, 04 Nov 2025 01:20:22 GMT  
		Size: 304.7 MB (304672762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86be4a1a181e230e85c044a97f7b710551e6d3bf203afc1479aa8dec343df8c5`  
		Last Modified: Tue, 04 Nov 2025 01:20:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:3c7d0ddde8cb352b70fbdda3a78f3771649ae2c9f239e1e087a2daf3d1323e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bed5c4f013812b64b7b7548c810216a9414373d254e64202f69f68d1d0a727`

```dockerfile
```

-	Layers:
	-	`sha256:dfb9bdbb320e3971cda2c08a579290fd64f4f60838c198d9965b3894cc1fd437`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651226e0dd9d108de2bd4156ffe234f9d2c9ca527fae2c31797ab0d56e9bd622`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; 386

```console
$ docker pull julia@sha256:d0b9d84847198bf7fa4453e2efe114db22eece072ba127bd4bdad755b21ab5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0b9670cd872909a31e44da8896181024f3a6554924009bcbb1d2141b18ee13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c4b44632242d439bd005ebb4d6616cd3a08772d224b9b7502af79bdf4b68`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 6.4 MB (6427799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1daf36fab91b2c580863fb421e918de2ded562304042a54df48addeffd07e1`  
		Last Modified: Tue, 04 Nov 2025 01:20:37 GMT  
		Size: 237.6 MB (237589306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26e42ea4da86b177c44034edbaee4d859f9d0ab93359709663e5b17845d431`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:ad35efca310a83724a463f62361641c237dfd0378d58193f57b4fd3549454149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968db347a32b2121fad86e5bb44a227a1fd3fbaa351e2f0b4dd37bf7a8fe2001`

```dockerfile
```

-	Layers:
	-	`sha256:3fd63a11e5039d0d9fd4fc07a7da6491e5279e6aaa6374d76d917440d26cffc2`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf1b6e8427f90711ea68122baffe32232ee2406c2d466e6bd28623f5ce8e6fb`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; ppc64le

```console
$ docker pull julia@sha256:af47fb9d083edb11b690b7a11bad7359b5a825e53e17355ce33e5e36aeb1723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd7daae7a851023d0e7ba4bfcb25275c9cf4e771c4b29c79cc666f417b2c309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:43:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804e3fa9e2b6d927adbfa2f484f29c48dfa02fa48ae6053634015859c5e44bd6`  
		Last Modified: Tue, 04 Nov 2025 01:45:10 GMT  
		Size: 248.6 MB (248575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59577986c334ac00b0537217cf3e085fba567d1ca11371d7d1f6e6e51bcc01`  
		Last Modified: Tue, 04 Nov 2025 01:45:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:8d43151df46a2c7140ba113af82ac260984f5cdafa2d1aa3dd9a7a2d321c207a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5817953051e2c01f0b487428d6642914ca32726c040f3030dfd8d467629ae7`

```dockerfile
```

-	Layers:
	-	`sha256:e9ea77425e0dd2f93981c3f6e5a450d1db4f1dc4572401f3b7964e76845874f7`  
		Last Modified: Tue, 04 Nov 2025 09:03:05 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7a3c3343500104211cda157133385e0318084ee640711be6d3e6a8ed21690e`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:3e4b6f02eb3db1f6f7fef665b79b647bd37482922c5bd8a39fc708700f6fe84e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49ef7f991db05bb94358171660b480fc0d722a820dca21a283c76a99f9c7204`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:13:08 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf1bb93f61e8c24fd4e2b3d6e7c1a7943daee471638a5102faccf0d22074f09`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d22a566df8f51c2575151699d1be7aded51355ae1069d6af81823f790845c7`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d376dc10fa6d5e6059e0f1c0458cf2f4a223cc933933219de01bc9d41f882c`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988b521dc749bef6ad5f6bd2bb5db65fb89261ab2f61aafad478ae081e56571`  
		Last Modified: Fri, 24 Oct 2025 20:03:28 GMT  
		Size: 286.0 MB (286040248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f857510290685f39eba099823626c8691f0e82156ca14232c875a5d04cee0cc6`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:3fd4821b551758c3327c024812ef254c02fccf931c0f149e703ef745a873d9e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863360535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c1c7e41c981d2d881f5280ed35b21cb891d6df13f80c5dbadd26a513273967`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b16e8884054f88f5b487e2736f79d2954386da590bb81cb5d157d5a32f0f6a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc97c885b2f12dc27a3f7692682304abf5cec4dca32d7105ed1e2c395c460f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e6a67941039a29b42f6001a5508703e7c5c84c75be187b38ca35f648d1768`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573a7892a8d07b89b24a2cb6ac382cb5e310149f59ad0bb2009ccc4cb665f2a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d057c66fb4ace98f74ecd96c641e284c587bd5071339e8c0b47e5e91713a76`  
		Last Modified: Fri, 24 Oct 2025 20:04:02 GMT  
		Size: 286.2 MB (286161015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bfd8c3a8e1bf28c28bcf735b62a68e683820c2450b6278ee68fab3bd28440`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-bookworm`

```console
$ docker pull julia@sha256:2634749aa561c40e9ccc10bce1d63a2623ef932d6f6bd74e33eee9b02dbc1df9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.7-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:a2fe0230f127a23f688122ffde0dd7328c55ac5abdc12b360a1118f4a4f9809b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8f3018decd8c10a81d1829ebb3c9ba98903a27aef46a930508307a2b963dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:18:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:18:58 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:18:58 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:18:58 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:18:58 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 00:18:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:18:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:18:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:18:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0dfad91cddb56b269dd4265bff9adb9b968d1c56c89241fe585d73572306d2`  
		Last Modified: Tue, 04 Nov 2025 00:19:50 GMT  
		Size: 5.7 MB (5716353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ef9c9497633959219112e8f0da9221b46d7fa94def22e71ab58e4de924b039`  
		Last Modified: Tue, 04 Nov 2025 10:56:24 GMT  
		Size: 288.8 MB (288788397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bf51bf4728bf1dbae8d828dfa99fdab9ef0f956e4af2e4843dfacadc6f993b`  
		Last Modified: Tue, 04 Nov 2025 00:19:49 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c00fc06fe8ac263b8606cbb9a83e61eaf38b57c2913a727db8ed42bbc87a8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c5d4f537d6162002130dc9ef35297e503974412f8938b29ea34e28d17cc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:932f9013aa1207eb422105ff1dc02fee44727414af05f7e2c9a70b2cb63c06c8`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f49e1730c5fb92267f29b860f3442112ce35e8e3a1f28c2f6738fcb89bc9cce`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2a8bede234d41d0f94259d2351d4c4568d0d3716c47711ef37ceaf917b0838e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5c71b8f02318901391800db522c443b104a331183a997a5f256157d6d7d4ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:19:16 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:19:16 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:19:16 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:19:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 00:19:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:19:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:19:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:19:16 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fd30e2e96bd67e71de351f0a116cd53aec6bf644d0116f902fc59868bba065`  
		Last Modified: Tue, 04 Nov 2025 00:20:18 GMT  
		Size: 5.6 MB (5567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c037fffe78b941f610f3b4982b1f837f57f07a2d8b2902b51b7c90f67b2418`  
		Last Modified: Tue, 04 Nov 2025 00:20:08 GMT  
		Size: 304.6 MB (304646620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07d07b723d472689e559c347328896264c36f5e1ec6d927e17fbc954cebbfdc`  
		Last Modified: Tue, 04 Nov 2025 00:20:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:611d957b656a75d051f322ce53e6e21cd2a951bc4ad320a533b0dbb650eaa35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee19cf5f710dca293dab6d0e2310873aae6dccc6702258b16a8854a1a4d65c2e`

```dockerfile
```

-	Layers:
	-	`sha256:2b84519d466535234c7b5055d976677cbbc9eae041c214964088acbf1de2eade`  
		Last Modified: Tue, 04 Nov 2025 12:03:22 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e86b6e2662fd1b1299cdb8b36344b6c0fce8718e112fb2deabaefdce3624a7c`  
		Last Modified: Tue, 04 Nov 2025 12:03:25 GMT  
		Size: 16.7 KB (16678 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:ad1f215325548359ca1f57fda6ba0cd638621f8b28ab318f6b1ab3196011eeb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272644005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6563ff2d41e29147321dfa66b88666c62a23c210c8853ffce3a19bd4495c32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:44 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:44 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:44 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:44 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 00:16:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d04fdc9b583a90fae6ec25b6bb90ea916644cd2a3c783251d14bbaa59db246`  
		Last Modified: Tue, 04 Nov 2025 00:17:50 GMT  
		Size: 5.9 MB (5878043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c917cc869a978d2e1cdac0e3c181898c15669a9358dbc98875f13aae34dce00e`  
		Last Modified: Tue, 04 Nov 2025 00:17:24 GMT  
		Size: 237.6 MB (237555746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c3466306423d1e76b5f8cc0bff2a744960f44b64597382de8df3572fe46c12`  
		Last Modified: Tue, 04 Nov 2025 00:17:50 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:5be748747d7a159189e996d25f19ba3ad772900a1bc32e7a40377f9088d3cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc3d49d001f84f5006065b8107684fd28eb43a9d54c3af38c74473af0b90126`

```dockerfile
```

-	Layers:
	-	`sha256:fa4523ff217295caccc18459923699b70721b17c199ad7371860c7e532616883`  
		Last Modified: Tue, 04 Nov 2025 12:03:28 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ae0f1a4a0fa0f1549b411797551910075f2ab2fb076166ed67a841318b04d0c`  
		Last Modified: Tue, 04 Nov 2025 12:03:29 GMT  
		Size: 16.6 KB (16559 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:ee59c2dff4a5dbbab3fb3f333fec5887c9b9d7233d98ef628b0cec97d378d000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c6f6bfa81dc86a6798fb3f5015ccf4c0ff7ca6661362ab341452e571c31161f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:46:35 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:46:35 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:46:35 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:46:35 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:46:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:46:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:46:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:46:35 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100319a5fe2f62c408488b2652211045c6a4b819d76492b9ffce2f37abb9ba00`  
		Last Modified: Tue, 04 Nov 2025 01:48:02 GMT  
		Size: 6.3 MB (6256339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e673a344de582bf81f4cf828559313cbaa253124528d26c65c9e56283c0d00c7`  
		Last Modified: Tue, 04 Nov 2025 01:47:55 GMT  
		Size: 248.6 MB (248553781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5facd3c79b38c0ef21d97c2a0005bc5d07496e0c3b714da014de64d7af279ea8`  
		Last Modified: Tue, 04 Nov 2025 01:48:01 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:f0dce5c9ddc2c4debdb683133976ae30975dd94a706e69821de44d55d8603595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2855d2c1f1953b5fae2e9fa8202910f64f0dce318728d0b94a42167874116c`

```dockerfile
```

-	Layers:
	-	`sha256:8322998454ca23430e1103826490dffb82114bbd02ded45435ee184f05ad8630`  
		Last Modified: Tue, 04 Nov 2025 09:03:16 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8a94bdd45295600accfc923ee1509e5ae779d21db84deb8c2546eaf2fd1db2`  
		Last Modified: Tue, 04 Nov 2025 09:03:17 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-trixie`

```console
$ docker pull julia@sha256:0bb482133691815f3c5f7da53758f9e12902f713286382b17ac4e41d1e04f018
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `julia:1.11.7-trixie` - linux; amd64

```console
$ docker pull julia@sha256:6221aee6839236bb4d2252758931755a84fb7b6fa47c3b194ea4c51585f03fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324846836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b57b9e4ac3820f22f9e8cceb5f60d41ed4a3081fa08a9aa610c5fac0ff447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:41 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 04:05:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06408e36a7e1d73b96137de5bd71a78afb2ce588d6cd94b57dae5b78ad9d4948`  
		Last Modified: Tue, 04 Nov 2025 04:06:34 GMT  
		Size: 6.2 MB (6242838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587e6cdd48a9666f4057b7a1006373d8006398052be9cbb55b7d8d95ec461a66`  
		Last Modified: Tue, 04 Nov 2025 09:10:51 GMT  
		Size: 288.8 MB (288825525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96191142a13dce96425c47257e8e0733fe4729b8733b5989dca96384458c843e`  
		Last Modified: Tue, 04 Nov 2025 04:06:33 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:8ff24e1f58421f64c451467350f044c2cdec90316bab6588d98e10446143e29c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b424ed2184a8bbaf12f7a112609faaa2208b5bbabafdbf269835ddb96c218646`

```dockerfile
```

-	Layers:
	-	`sha256:41ce5b3eb055a8dd7cc5be314e1f5f0ec46e20e5886d253771f76b579abb3711`  
		Last Modified: Tue, 04 Nov 2025 09:02:55 GMT  
		Size: 2.2 MB (2238915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:142507089fe0778974555b71bc47ec0a3c0dec3255adf7bfe9cb83cae1fd61ae`  
		Last Modified: Tue, 04 Nov 2025 09:02:56 GMT  
		Size: 17.2 KB (17151 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:dd0a2471c77bc81d4b77c7279d9982dd87d4a92d65cf2f4865f3bb3e469d62f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340968507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f325fd60152ce42b1e02f5021518978f1fe205a1745a217d479b5f65059f37a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:31 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a17ece07a394ffce3a2ea1e4714b628c8bf0d7c1629223d158c65c3990d10c`  
		Last Modified: Tue, 04 Nov 2025 01:20:29 GMT  
		Size: 6.2 MB (6153077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe73bac822b894e42e6cb67af04484131a8b4bc33e7e87591e151a35df4de147`  
		Last Modified: Tue, 04 Nov 2025 01:20:22 GMT  
		Size: 304.7 MB (304672762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86be4a1a181e230e85c044a97f7b710551e6d3bf203afc1479aa8dec343df8c5`  
		Last Modified: Tue, 04 Nov 2025 01:20:28 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:3c7d0ddde8cb352b70fbdda3a78f3771649ae2c9f239e1e087a2daf3d1323e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bed5c4f013812b64b7b7548c810216a9414373d254e64202f69f68d1d0a727`

```dockerfile
```

-	Layers:
	-	`sha256:dfb9bdbb320e3971cda2c08a579290fd64f4f60838c198d9965b3894cc1fd437`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 2.2 MB (2239199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:651226e0dd9d108de2bd4156ffe234f9d2c9ca527fae2c31797ab0d56e9bd622`  
		Last Modified: Tue, 04 Nov 2025 12:03:15 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; 386

```console
$ docker pull julia@sha256:d0b9d84847198bf7fa4453e2efe114db22eece072ba127bd4bdad755b21ab5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275312259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0b9670cd872909a31e44da8896181024f3a6554924009bcbb1d2141b18ee13`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:57 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:57 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9538c4b44632242d439bd005ebb4d6616cd3a08772d224b9b7502af79bdf4b68`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 6.4 MB (6427799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1daf36fab91b2c580863fb421e918de2ded562304042a54df48addeffd07e1`  
		Last Modified: Tue, 04 Nov 2025 01:20:37 GMT  
		Size: 237.6 MB (237589306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26e42ea4da86b177c44034edbaee4d859f9d0ab93359709663e5b17845d431`  
		Last Modified: Tue, 04 Nov 2025 01:20:43 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:ad35efca310a83724a463f62361641c237dfd0378d58193f57b4fd3549454149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968db347a32b2121fad86e5bb44a227a1fd3fbaa351e2f0b4dd37bf7a8fe2001`

```dockerfile
```

-	Layers:
	-	`sha256:3fd63a11e5039d0d9fd4fc07a7da6491e5279e6aaa6374d76d917440d26cffc2`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 2.2 MB (2236060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf1b6e8427f90711ea68122baffe32232ee2406c2d466e6bd28623f5ce8e6fb`  
		Last Modified: Tue, 04 Nov 2025 12:03:19 GMT  
		Size: 17.1 KB (17117 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; ppc64le

```console
$ docker pull julia@sha256:af47fb9d083edb11b690b7a11bad7359b5a825e53e17355ce33e5e36aeb1723d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.9 MB (288857162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd7daae7a851023d0e7ba4bfcb25275c9cf4e771c4b29c79cc666f417b2c309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:43:51 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:43:51 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 04 Nov 2025 01:43:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:43:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:43:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85dc345bbaec013d0af1b3a0829581e4ee9cb2e7d49e55cd93687b4c475b2a30`  
		Last Modified: Tue, 04 Nov 2025 01:45:27 GMT  
		Size: 6.7 MB (6682211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804e3fa9e2b6d927adbfa2f484f29c48dfa02fa48ae6053634015859c5e44bd6`  
		Last Modified: Tue, 04 Nov 2025 01:45:10 GMT  
		Size: 248.6 MB (248575936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed59577986c334ac00b0537217cf3e085fba567d1ca11371d7d1f6e6e51bcc01`  
		Last Modified: Tue, 04 Nov 2025 01:45:26 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:8d43151df46a2c7140ba113af82ac260984f5cdafa2d1aa3dd9a7a2d321c207a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2259841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e5817953051e2c01f0b487428d6642914ca32726c040f3030dfd8d467629ae7`

```dockerfile
```

-	Layers:
	-	`sha256:e9ea77425e0dd2f93981c3f6e5a450d1db4f1dc4572401f3b7964e76845874f7`  
		Last Modified: Tue, 04 Nov 2025 09:03:05 GMT  
		Size: 2.2 MB (2242644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a7a3c3343500104211cda157133385e0318084ee640711be6d3e6a8ed21690e`  
		Last Modified: Tue, 04 Nov 2025 09:03:06 GMT  
		Size: 17.2 KB (17197 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-windowsservercore`

```console
$ docker pull julia@sha256:7583e7051f75688be7143960b83180a73b4d1433393614307e9fbd7e3eac56c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.11.7-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:3e4b6f02eb3db1f6f7fef665b79b647bd37482922c5bd8a39fc708700f6fe84e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49ef7f991db05bb94358171660b480fc0d722a820dca21a283c76a99f9c7204`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:13:08 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf1bb93f61e8c24fd4e2b3d6e7c1a7943daee471638a5102faccf0d22074f09`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d22a566df8f51c2575151699d1be7aded51355ae1069d6af81823f790845c7`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d376dc10fa6d5e6059e0f1c0458cf2f4a223cc933933219de01bc9d41f882c`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988b521dc749bef6ad5f6bd2bb5db65fb89261ab2f61aafad478ae081e56571`  
		Last Modified: Fri, 24 Oct 2025 20:03:28 GMT  
		Size: 286.0 MB (286040248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f857510290685f39eba099823626c8691f0e82156ca14232c875a5d04cee0cc6`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:3fd4821b551758c3327c024812ef254c02fccf931c0f149e703ef745a873d9e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863360535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c1c7e41c981d2d881f5280ed35b21cb891d6df13f80c5dbadd26a513273967`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b16e8884054f88f5b487e2736f79d2954386da590bb81cb5d157d5a32f0f6a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc97c885b2f12dc27a3f7692682304abf5cec4dca32d7105ed1e2c395c460f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e6a67941039a29b42f6001a5508703e7c5c84c75be187b38ca35f648d1768`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573a7892a8d07b89b24a2cb6ac382cb5e310149f59ad0bb2009ccc4cb665f2a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d057c66fb4ace98f74ecd96c641e284c587bd5071339e8c0b47e5e91713a76`  
		Last Modified: Fri, 24 Oct 2025 20:04:02 GMT  
		Size: 286.2 MB (286161015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bfd8c3a8e1bf28c28bcf735b62a68e683820c2450b6278ee68fab3bd28440`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:3a20f9c4936f8e6603f2dd59188d3bdc3e043b9758a946b77fdaca90c6d18e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1.11.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:3fd4821b551758c3327c024812ef254c02fccf931c0f149e703ef745a873d9e0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1863360535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c1c7e41c981d2d881f5280ed35b21cb891d6df13f80c5dbadd26a513273967`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b16e8884054f88f5b487e2736f79d2954386da590bb81cb5d157d5a32f0f6a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc97c885b2f12dc27a3f7692682304abf5cec4dca32d7105ed1e2c395c460f`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883e6a67941039a29b42f6001a5508703e7c5c84c75be187b38ca35f648d1768`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4573a7892a8d07b89b24a2cb6ac382cb5e310149f59ad0bb2009ccc4cb665f2a`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d057c66fb4ace98f74ecd96c641e284c587bd5071339e8c0b47e5e91713a76`  
		Last Modified: Fri, 24 Oct 2025 20:04:02 GMT  
		Size: 286.2 MB (286161015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6bfd8c3a8e1bf28c28bcf735b62a68e683820c2450b6278ee68fab3bd28440`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:1d13bb74b64576b845b13bb0cd9f284ed2927b75732a5fcece2160c97100cd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1.11.7-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:3e4b6f02eb3db1f6f7fef665b79b647bd37482922c5bd8a39fc708700f6fe84e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3506393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49ef7f991db05bb94358171660b480fc0d722a820dca21a283c76a99f9c7204`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_VERSION=1.11.7
# Fri, 24 Oct 2025 18:13:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Fri, 24 Oct 2025 18:13:08 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Fri, 24 Oct 2025 18:14:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9235cc3c3cb68485c33877f779011c5a8c97c24f91de0e5999d9885837e759`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf1bb93f61e8c24fd4e2b3d6e7c1a7943daee471638a5102faccf0d22074f09`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d22a566df8f51c2575151699d1be7aded51355ae1069d6af81823f790845c7`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d376dc10fa6d5e6059e0f1c0458cf2f4a223cc933933219de01bc9d41f882c`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d988b521dc749bef6ad5f6bd2bb5db65fb89261ab2f61aafad478ae081e56571`  
		Last Modified: Fri, 24 Oct 2025 20:03:28 GMT  
		Size: 286.0 MB (286040248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f857510290685f39eba099823626c8691f0e82156ca14232c875a5d04cee0cc6`  
		Last Modified: Fri, 24 Oct 2025 18:22:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12`

```console
$ docker pull julia@sha256:6988944c178fa71f4fb0548281fc6dc5c454a3231021d0f3f3c7b1b98a7be136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.12` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-bookworm`

```console
$ docker pull julia@sha256:3aae05f9821c507b842d87ce7a83725c4467edaf4d4ae3bf623b8ff07004b05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:500372ec6ab9741301c27e345cc7e6708946b36de0216c3b3e6239a163c9b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5997a30c10df568c491bbe08a95a45b19abeb886af268909f72ffdeef3f22a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ace6d66d3a3d6fad5a1bd31565e9c119574e312dbf2c55d7ced0a4d992e9`  
		Last Modified: Tue, 04 Nov 2025 00:18:36 GMT  
		Size: 5.7 MB (5716426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d378682861b91f1053d2a1d43464b2e57b6395f94b5f3616162773b305beb7a`  
		Last Modified: Tue, 04 Nov 2025 10:36:01 GMT  
		Size: 289.5 MB (289470929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b061c9f75eba30cf7b20f413cee1eb00a9792af624a81cc98ae89703a73af6f`  
		Last Modified: Tue, 04 Nov 2025 00:18:35 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0f2ade0b8ea9e16026159dd251a169c750b2036fadf23fa790173f5786abef5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca9af7418798601cc04f6d6a48739a9a5da2a2e8482a07a023fdcf69ec0087`

```dockerfile
```

-	Layers:
	-	`sha256:a1ca6642d24f5181480f5bb0515421c6f570b5abdbe45693da59426dc16c0569`  
		Last Modified: Tue, 04 Nov 2025 09:03:26 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f2b8bfcd164157a77616ff0c66cd57015fb0f62d644a857a0f0afae188278b`  
		Last Modified: Tue, 04 Nov 2025 09:03:27 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4dfad4c810fdc31ae725d248983cbefbae1df3f6bdb6b4e944002a94a68c36bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06ec30bbfc55e57787d9f31eca6b80846748ef0363c4f9fcfe81df203ef0ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7199a6c929b6d0910d53e32159d8d4a96b2bbfe63afacda8c1e08bb035462`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 5.6 MB (5567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05efc5faad78e038dbe03bd02c615e0b76965f7a8a490e504f4ce7d87b612e`  
		Last Modified: Tue, 04 Nov 2025 00:18:39 GMT  
		Size: 310.2 MB (310205326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47e0b771b47e33a97f9e83589db5a6704058ee4a6d0ebb2ea3a58608487de5`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b9e05a0cbe438b70a93dad310acf8080004bb3a3f8711d4e8bcc09dbccb5a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393cbcc803f86aaa5f4ca3e66fd98503eff8f9899ec570fa2a2ab4b339456db6`

```dockerfile
```

-	Layers:
	-	`sha256:1489217e1ad8fa0212b331b460f9a9d4179d0e0f91f2678e1584d337977e1ed8`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdd4101aa2f92fb683b0ade00736d7f9febb97dbdc1620c2437587dde528473`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b7b2aa64a703e070f3336775ca69c137d785eb8700ae65f77cc0e6b759ee5d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312d4d17eebcf8fa147335c9eb1528fb268c227023f969103062ea8fe0c5830f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed679b54c5167ee52acb091f4d82f3b6acbafe02cddb714ebae4a0595a28f4`  
		Last Modified: Tue, 04 Nov 2025 00:17:28 GMT  
		Size: 5.9 MB (5878102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c583711dbb5e1bcb432195e396db5b8c27f36cd377de394faa956eeafaef9c9`  
		Last Modified: Tue, 04 Nov 2025 00:17:14 GMT  
		Size: 231.0 MB (231003092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c81c730697f6e563baad7c504576c729ef56d9082d11989882c45b83572fc2`  
		Last Modified: Tue, 04 Nov 2025 00:17:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:590ef71cd93f47132cdb712b908065edb792a5d2740d059f9f901bff40f74e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7354b4e55ca63d4fd0ac996a59834e68b1bbee3310e2b7777d6a6693583b56f5`

```dockerfile
```

-	Layers:
	-	`sha256:5dbc38afd08e09a5287ae9337d8aac4c769864909ee65694125473f54b9ee8fc`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5546efb59869a678415785da134451168dcd6768ff70c4cd0481388882aecd5b`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-trixie`

```console
$ docker pull julia@sha256:ac48e8257c839954341858486babc1e1ec1ec61c137577dba475a4de1bcf257c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12-trixie` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-windowsservercore`

```console
$ docker pull julia@sha256:37c56bf72faa4943f68f85317d46d634b09f9f80d8eb60a56c5b43a4a10ef152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.12-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1373ec157b80534a185f04456f792e25f678f6fd3ba7c1c90e5df512f1d6eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fa10c1c8c32867203dde7a7be57b7e184bda0c46e4bfd0fa4054e4abd8ca9d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1.12-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1`

```console
$ docker pull julia@sha256:6988944c178fa71f4fb0548281fc6dc5c454a3231021d0f3f3c7b1b98a7be136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.12.1` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.1` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-bookworm`

```console
$ docker pull julia@sha256:3aae05f9821c507b842d87ce7a83725c4467edaf4d4ae3bf623b8ff07004b05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.1-bookworm` - linux; amd64

```console
$ docker pull julia@sha256:500372ec6ab9741301c27e345cc7e6708946b36de0216c3b3e6239a163c9b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5997a30c10df568c491bbe08a95a45b19abeb886af268909f72ffdeef3f22a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ace6d66d3a3d6fad5a1bd31565e9c119574e312dbf2c55d7ced0a4d992e9`  
		Last Modified: Tue, 04 Nov 2025 00:18:36 GMT  
		Size: 5.7 MB (5716426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d378682861b91f1053d2a1d43464b2e57b6395f94b5f3616162773b305beb7a`  
		Last Modified: Tue, 04 Nov 2025 10:36:01 GMT  
		Size: 289.5 MB (289470929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b061c9f75eba30cf7b20f413cee1eb00a9792af624a81cc98ae89703a73af6f`  
		Last Modified: Tue, 04 Nov 2025 00:18:35 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0f2ade0b8ea9e16026159dd251a169c750b2036fadf23fa790173f5786abef5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca9af7418798601cc04f6d6a48739a9a5da2a2e8482a07a023fdcf69ec0087`

```dockerfile
```

-	Layers:
	-	`sha256:a1ca6642d24f5181480f5bb0515421c6f570b5abdbe45693da59426dc16c0569`  
		Last Modified: Tue, 04 Nov 2025 09:03:26 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f2b8bfcd164157a77616ff0c66cd57015fb0f62d644a857a0f0afae188278b`  
		Last Modified: Tue, 04 Nov 2025 09:03:27 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4dfad4c810fdc31ae725d248983cbefbae1df3f6bdb6b4e944002a94a68c36bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06ec30bbfc55e57787d9f31eca6b80846748ef0363c4f9fcfe81df203ef0ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7199a6c929b6d0910d53e32159d8d4a96b2bbfe63afacda8c1e08bb035462`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 5.6 MB (5567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05efc5faad78e038dbe03bd02c615e0b76965f7a8a490e504f4ce7d87b612e`  
		Last Modified: Tue, 04 Nov 2025 00:18:39 GMT  
		Size: 310.2 MB (310205326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47e0b771b47e33a97f9e83589db5a6704058ee4a6d0ebb2ea3a58608487de5`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b9e05a0cbe438b70a93dad310acf8080004bb3a3f8711d4e8bcc09dbccb5a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393cbcc803f86aaa5f4ca3e66fd98503eff8f9899ec570fa2a2ab4b339456db6`

```dockerfile
```

-	Layers:
	-	`sha256:1489217e1ad8fa0212b331b460f9a9d4179d0e0f91f2678e1584d337977e1ed8`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdd4101aa2f92fb683b0ade00736d7f9febb97dbdc1620c2437587dde528473`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:b7b2aa64a703e070f3336775ca69c137d785eb8700ae65f77cc0e6b759ee5d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312d4d17eebcf8fa147335c9eb1528fb268c227023f969103062ea8fe0c5830f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed679b54c5167ee52acb091f4d82f3b6acbafe02cddb714ebae4a0595a28f4`  
		Last Modified: Tue, 04 Nov 2025 00:17:28 GMT  
		Size: 5.9 MB (5878102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c583711dbb5e1bcb432195e396db5b8c27f36cd377de394faa956eeafaef9c9`  
		Last Modified: Tue, 04 Nov 2025 00:17:14 GMT  
		Size: 231.0 MB (231003092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c81c730697f6e563baad7c504576c729ef56d9082d11989882c45b83572fc2`  
		Last Modified: Tue, 04 Nov 2025 00:17:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:590ef71cd93f47132cdb712b908065edb792a5d2740d059f9f901bff40f74e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7354b4e55ca63d4fd0ac996a59834e68b1bbee3310e2b7777d6a6693583b56f5`

```dockerfile
```

-	Layers:
	-	`sha256:5dbc38afd08e09a5287ae9337d8aac4c769864909ee65694125473f54b9ee8fc`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5546efb59869a678415785da134451168dcd6768ff70c4cd0481388882aecd5b`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.1-trixie`

```console
$ docker pull julia@sha256:ac48e8257c839954341858486babc1e1ec1ec61c137577dba475a4de1bcf257c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:1.12.1-trixie` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-trixie` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.1-windowsservercore`

```console
$ docker pull julia@sha256:37c56bf72faa4943f68f85317d46d634b09f9f80d8eb60a56c5b43a4a10ef152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:1.12.1-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.1-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1373ec157b80534a185f04456f792e25f678f6fd3ba7c1c90e5df512f1d6eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:1.12.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fa10c1c8c32867203dde7a7be57b7e184bda0c46e4bfd0fa4054e4abd8ca9d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:1.12.1-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:3aae05f9821c507b842d87ce7a83725c4467edaf4d4ae3bf623b8ff07004b05b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:bookworm` - linux; amd64

```console
$ docker pull julia@sha256:500372ec6ab9741301c27e345cc7e6708946b36de0216c3b3e6239a163c9b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5997a30c10df568c491bbe08a95a45b19abeb886af268909f72ffdeef3f22a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:41 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:41 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ace6d66d3a3d6fad5a1bd31565e9c119574e312dbf2c55d7ced0a4d992e9`  
		Last Modified: Tue, 04 Nov 2025 00:18:36 GMT  
		Size: 5.7 MB (5716426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d378682861b91f1053d2a1d43464b2e57b6395f94b5f3616162773b305beb7a`  
		Last Modified: Tue, 04 Nov 2025 10:36:01 GMT  
		Size: 289.5 MB (289470929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b061c9f75eba30cf7b20f413cee1eb00a9792af624a81cc98ae89703a73af6f`  
		Last Modified: Tue, 04 Nov 2025 00:18:35 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:0f2ade0b8ea9e16026159dd251a169c750b2036fadf23fa790173f5786abef5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ca9af7418798601cc04f6d6a48739a9a5da2a2e8482a07a023fdcf69ec0087`

```dockerfile
```

-	Layers:
	-	`sha256:a1ca6642d24f5181480f5bb0515421c6f570b5abdbe45693da59426dc16c0569`  
		Last Modified: Tue, 04 Nov 2025 09:03:26 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f2b8bfcd164157a77616ff0c66cd57015fb0f62d644a857a0f0afae188278b`  
		Last Modified: Tue, 04 Nov 2025 09:03:27 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4dfad4c810fdc31ae725d248983cbefbae1df3f6bdb6b4e944002a94a68c36bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06ec30bbfc55e57787d9f31eca6b80846748ef0363c4f9fcfe81df203ef0ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:17:48 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:17:48 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:17:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:17:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:17:48 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b7199a6c929b6d0910d53e32159d8d4a96b2bbfe63afacda8c1e08bb035462`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 5.6 MB (5567247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c05efc5faad78e038dbe03bd02c615e0b76965f7a8a490e504f4ce7d87b612e`  
		Last Modified: Tue, 04 Nov 2025 00:18:39 GMT  
		Size: 310.2 MB (310205326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47e0b771b47e33a97f9e83589db5a6704058ee4a6d0ebb2ea3a58608487de5`  
		Last Modified: Tue, 04 Nov 2025 00:18:46 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:b9e05a0cbe438b70a93dad310acf8080004bb3a3f8711d4e8bcc09dbccb5a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393cbcc803f86aaa5f4ca3e66fd98503eff8f9899ec570fa2a2ab4b339456db6`

```dockerfile
```

-	Layers:
	-	`sha256:1489217e1ad8fa0212b331b460f9a9d4179d0e0f91f2678e1584d337977e1ed8`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebdd4101aa2f92fb683b0ade00736d7f9febb97dbdc1620c2437587dde528473`  
		Last Modified: Tue, 04 Nov 2025 00:18:32 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:b7b2aa64a703e070f3336775ca69c137d785eb8700ae65f77cc0e6b759ee5d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312d4d17eebcf8fa147335c9eb1528fb268c227023f969103062ea8fe0c5830f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 00:16:39 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 00:16:39 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 00:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:39 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:e0dafb38d1608fdb0908090be60250d2f739b5a9191857a4c4a74ebd3ef3b814`  
		Last Modified: Tue, 04 Nov 2025 00:12:54 GMT  
		Size: 29.2 MB (29209846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed679b54c5167ee52acb091f4d82f3b6acbafe02cddb714ebae4a0595a28f4`  
		Last Modified: Tue, 04 Nov 2025 00:17:28 GMT  
		Size: 5.9 MB (5878102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c583711dbb5e1bcb432195e396db5b8c27f36cd377de394faa956eeafaef9c9`  
		Last Modified: Tue, 04 Nov 2025 00:17:14 GMT  
		Size: 231.0 MB (231003092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c81c730697f6e563baad7c504576c729ef56d9082d11989882c45b83572fc2`  
		Last Modified: Tue, 04 Nov 2025 00:17:27 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:590ef71cd93f47132cdb712b908065edb792a5d2740d059f9f901bff40f74e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7354b4e55ca63d4fd0ac996a59834e68b1bbee3310e2b7777d6a6693583b56f5`

```dockerfile
```

-	Layers:
	-	`sha256:5dbc38afd08e09a5287ae9337d8aac4c769864909ee65694125473f54b9ee8fc`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5546efb59869a678415785da134451168dcd6768ff70c4cd0481388882aecd5b`  
		Last Modified: Tue, 04 Nov 2025 00:17:10 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:6988944c178fa71f4fb0548281fc6dc5c454a3231021d0f3f3c7b1b98a7be136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:trixie`

```console
$ docker pull julia@sha256:ac48e8257c839954341858486babc1e1ec1ec61c137577dba475a4de1bcf257c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `julia:trixie` - linux; amd64

```console
$ docker pull julia@sha256:a6211212f9a233307bbac98c300d9e15147afa134a7c314d99556f328eaee80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325530956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b32e015f64408b7c02373ceaec20b17a7a88cdec947ecdcfbbb17b410abeef0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 04:05:36 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 04:05:36 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 04:05:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:05:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:05:36 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872696bc7859202e5d6d510e37ed0d8040b8a9733fd085dcf52044bdf5fe5567`  
		Last Modified: Tue, 04 Nov 2025 04:06:32 GMT  
		Size: 6.2 MB (6242778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba7bfc6d84638297b5a603f3aa2b029958790aba803a949d786ab231da90f0a`  
		Last Modified: Tue, 04 Nov 2025 09:07:59 GMT  
		Size: 289.5 MB (289509706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d050197dc9083456b1c225b9fcabd9f1018b50f06effaaf1ebb212f905d8d6e`  
		Last Modified: Tue, 04 Nov 2025 04:06:31 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b83b9ce77280a6a92a94a388238c391614a0822524f46bf234472beee332ebd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f747f805f93af69ac41fc456c0a4982380cb810f6abb3c3c2243e6b40336dee8`

```dockerfile
```

-	Layers:
	-	`sha256:35a29cbd11434f6fdb1a7845c123931da1b74787629f32a4ed644f4b764c8aa2`  
		Last Modified: Tue, 04 Nov 2025 09:03:32 GMT  
		Size: 2.2 MB (2240093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1b66cef3def3210eeda9d07a7a8a920e11e08a9f80fa97fba09414ee36cf61`  
		Last Modified: Tue, 04 Nov 2025 09:03:33 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ef1704f52f9d8d744aeac1ca3d76743f740f05880876b2243cf6d487c33cb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346539308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96908b89aeea3592b25425b975ee49e90470ac567cdc83bc39f60ffdc67bd9ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:20:06 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:20:06 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:20:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:20:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:20:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9594e474286a5bac97d719763020e93be96afb2dc29eb202edaa3362a78bab`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 6.2 MB (6153115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ce4d459beceb80d7c24b98c425c9f07106e98d2ea5c83d45f8b08a23a5df8`  
		Last Modified: Tue, 04 Nov 2025 01:20:59 GMT  
		Size: 310.2 MB (310243523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321e7d47551fb2a9c73dd7d72b93264d87a6339b6496ac5c0ac2146259e52b56`  
		Last Modified: Tue, 04 Nov 2025 01:21:05 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bb339ae4d18d2239e6de1b6e67fc48bf6f04ec6cf6fef4008f9ed83b5e097a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7145feccfd3abd2cd0c2719f3cf26e4b5ce171cb751ddec622738250bd366e9c`

```dockerfile
```

-	Layers:
	-	`sha256:98ec3993677aca37028d069b32ef3658f0eedc4c5f18041999efa89d9b257b12`  
		Last Modified: Tue, 04 Nov 2025 12:02:24 GMT  
		Size: 2.2 MB (2240425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd05cbf986c8ba4b88dbbc7924e67bb348686d4e14a0265f5f50079cab23ef94`  
		Last Modified: Tue, 04 Nov 2025 12:02:25 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:f698bc25145572e825fd10a55e6b228d042ee473fb411442b0b18ebe8b7eea9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268757057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8044b27c0a9e30851d8718009619fcc79bd3d20fb326d1b5f1e2ce5fff9702`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 04 Nov 2025 01:19:49 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 04 Nov 2025 01:19:49 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 04 Nov 2025 01:19:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:19:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:19:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa2d66fb1c3890569bc92b639d550036c9fc34d83671e1b10b332551a72385d`  
		Last Modified: Tue, 04 Nov 2025 01:20:32 GMT  
		Size: 6.4 MB (6427792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0acece2b51dbb22882d1ebd7badca729f8d8bae6a22c73e6b6373b3a9b759261`  
		Last Modified: Tue, 04 Nov 2025 01:20:26 GMT  
		Size: 231.0 MB (231034111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da2f9164d46b7f9c479754dd7c9bf471670fb3fda4d108a3f01011ff0a26fb6`  
		Last Modified: Tue, 04 Nov 2025 01:20:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:b0408b80aed11089df48d9c2c4e2555e8f568111da00b8616163a2daeca680c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a131e418a747d8671389549b5c82d554c16cd246124843c14b3b89f51f88d2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a6dd58d1d70f31d07cf44744c6f07965abd0000e277aa944560548cb5f27dc8c`  
		Last Modified: Tue, 04 Nov 2025 12:02:28 GMT  
		Size: 2.2 MB (2237218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2878a102b5c95b15c8aa6e0f74d8bf2e7d4c5e5e31ea9e3d92606b02ed057bbf`  
		Last Modified: Tue, 04 Nov 2025 12:02:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:37c56bf72faa4943f68f85317d46d634b09f9f80d8eb60a56c5b43a4a10ef152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `julia:windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1373ec157b80534a185f04456f792e25f678f6fd3ba7c1c90e5df512f1d6eb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull julia@sha256:58b4cc88e3880218b70059511b02b1ffa338f76d66417d36c45d24b5da934d01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1962105552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363572e4f390927b13f404e49177cb4d94c88fdad9a20fff9026c671964cde45`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:10:43 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:10:45 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:10:46 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:15:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:15:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9984184181e23d0dcb710166c08f49616136ae21c8cc1fdbede48bb702d85cec`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734b67fcbdce10dc9334ca4b1f797d4d2d2d86b43e54f884a66087b83ffc314`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269cbb3253ca381397377be291a0235375f06d55ced961a0a857fe9612da9f2e`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce413e76fc1a1ac17e1a4aaaaf44544e02e0af54b7cd7c91543cbe41ecff10b9`  
		Last Modified: Fri, 24 Oct 2025 20:02:40 GMT  
		Size: 384.9 MB (384906047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142dc4f4e79c09d549b4f47d7c68c9fdadb0b5ff2d0f85a5dc7041c945e5d253`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fa10c1c8c32867203dde7a7be57b7e184bda0c46e4bfd0fa4054e4abd8ca9d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
