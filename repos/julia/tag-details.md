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
$ docker pull julia@sha256:f1af93b4fcb73cb431b0ff0c1157d90f82e399a3f541fc5afbcd8e4b0778f35a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1` - linux; amd64

```console
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-bookworm`

```console
$ docker pull julia@sha256:a4be0555a49afd63319b87474c2abbc3bb39d189b91c7afcf880856a08ff2f43
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
$ docker pull julia@sha256:718fae8afcc3d82bee2d8e93b98d357fb91ce67143cd0b3db0eb0d30ad701999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e590adf2e6082fa367e7f681243a7ada431693170e3fbc95f98e267556edfc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:19:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:19:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6196f36242058df76aeed9f9be74444179b9361f55a75d95abce3f2073704`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 5.7 MB (5716358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c89fe608b9302afc559f89092749ddd8047d27f98c5ebab051be79706b58e0`  
		Last Modified: Tue, 18 Nov 2025 12:34:34 GMT  
		Size: 289.5 MB (289470935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba290a3255b38cfcf0e40d2b93602d7c0331965e96dada070859689deb832c2`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:07459013e718289defd96141a743741a998efd75d41d75077dcc86771b546c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534910b59c852b8c4cfeafef23e74a4fdf4514bccda123491b950bc4737db3ea`

```dockerfile
```

-	Layers:
	-	`sha256:ca2dbafbd8fd35f3cd8381ea4ac405b5cc3d725c3c325fa92acbf9fb08ce39ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8b8dc4394b9cfe5c43dd5231757832ea00f02c1fb0e2c68ac60e9b2ab00f69`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b52198fa87dc48d6231e6da93b220c6935033da0f857a20b2eb1f9152f6c0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff38f96d75673ca094cad57f9bd0b2a43173335b695ba04b16938979b4c5c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:21:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db58b4bbda4a603f718f99bd5c8e7d3ac963774cf121fc4d9d9ca8db27cf15`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 5.6 MB (5567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3242c924db6e3b513506ae3c10c101cd9fb859a2137367be3d0524546d3a3`  
		Last Modified: Tue, 18 Nov 2025 02:22:16 GMT  
		Size: 310.2 MB (310205363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c28b844f67c27a9f4854bff15183348e5b52fd5368f44ccd04398dc6d4f6f`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:549b77055b0192f55796e3e14f35fbe2d53d8a896c1ce0ef2657d6764f5a3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f920fa3c749e7d7c93d18ccfd01f56422aa2f989199cf61e98d847c7c1cfbe29`

```dockerfile
```

-	Layers:
	-	`sha256:3ca3f69c58a3d7a3bb4b975209b2de965c357469bbddfa2137163c277baa895b`  
		Last Modified: Tue, 18 Nov 2025 06:03:34 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e67e1e652d5f72a09dd04b91ae3e0fb4c37e3ea8c3ee16e99e03a3fd47cf8be`  
		Last Modified: Tue, 18 Nov 2025 06:03:35 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:71a6b70c3b3b6307e07b49e0f9ff1519bbb62ddd79126a7be07485bf7c14dae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0cfae68c743761541da4c76d24ab04e660427f0a4dc013baf72fd5aa08de0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:15:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2637d647fce9b735bc6ad4f3ef61b077daf59496f8bc5511b70af849249a2`  
		Last Modified: Tue, 18 Nov 2025 02:16:17 GMT  
		Size: 5.9 MB (5878089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3982f26c9084dc73e80d5e7bf8913a086c4dd9a22462ecd4f65de4c9d33dfa5`  
		Last Modified: Tue, 18 Nov 2025 02:16:10 GMT  
		Size: 231.0 MB (231003052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfb666991d4489bbf89a6f45668e810b3c45f39ef4a1464a0c42e4a47756060`  
		Last Modified: Tue, 18 Nov 2025 02:16:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:999d6ffcb86b5e482c6453855c55eb2f9bf0200938fdd2b9b00861b8c0be5fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0a9eb7698dbbbaf62ac2c022f559cc5ffb7ff52b19c9d0ae783b0337802d7`

```dockerfile
```

-	Layers:
	-	`sha256:1c44b469d322786f4c8698d066fcb0f246eb8df23db3663daff8029e6347a6f9`  
		Last Modified: Tue, 18 Nov 2025 06:03:39 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24641a1bf618df92a443bf98472b79166c077d32e94b2077eb51c0c3ef9ee6ee`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-trixie`

```console
$ docker pull julia@sha256:ff69f979004f8191acdfb9168ed8fa53d60b7fd2b6f2154fc24aa1cf196ad1be
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
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1-trixie` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:9b2cf26780ab0598b31c3d1b8a5163541515aa48c1615e76d6f4f65b5ae98a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:262db25a6585488ac281d30d018524c7a4dfc7a63fd5d0e9182cbb4c0a5579d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:5a6c083eb99ca2fe16b1308c41034455704607d80b32c8f30a8f3348e4a4737a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10`

```console
$ docker pull julia@sha256:70ac1a43be2ee61dc22dbb3d51a41ef0dad18be2dc42dcbf6d1e3ee56aa1f5a4
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
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10` - linux; amd64

```console
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
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

### `julia:1.10` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
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
$ docker pull julia@sha256:5381d01c3615422f73fde38e729f1817068c6b5bab9160ba2d98b243b352217f
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
$ docker pull julia@sha256:299c3c8333df7a50dcd02ebccef345b1f88048f6c7d892001481cd378c5d46cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c18876753015f55ad8389bc1856f4d5d847bfbadb6b3146d0b023332bbeca92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:22:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:22:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be4ab744883e883a44090eab187db08ad07885ee0d0e0a30d296c508fb12ba`  
		Last Modified: Tue, 18 Nov 2025 04:23:25 GMT  
		Size: 5.7 MB (5716399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686df9e4f2726cc605d0bb4489f6b0259b3b543877e935cd58c1183252aa4b21`  
		Last Modified: Tue, 18 Nov 2025 06:11:30 GMT  
		Size: 176.3 MB (176324443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061c64217926f23766909405893cb28a9640e36e487fbc69b8eb50a226575d2`  
		Last Modified: Tue, 18 Nov 2025 04:23:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9174cb7321d5fb61b395fd1388ace0d42af55407c54f50a81b74f66515b9bdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4d25e0e4acc0b84213fc7c5f7bae960ae76aeac5a4ec60332e591ace7ba26`

```dockerfile
```

-	Layers:
	-	`sha256:18a0814e0c9aa4c785962304e74d9d35451f6f8e418467e8091daa6af258b9c7`  
		Last Modified: Tue, 18 Nov 2025 06:03:57 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da5bbba4e084f79beb08d7b46c9429e44212f1262b14763c5f4716f4ae8d715`  
		Last Modified: Tue, 18 Nov 2025 06:03:58 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2f54cb3c7b23e9497c60cacc75eaef83da3df5a0f7fc96e467ad90b141df7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e0059c86daa089e2f731ea3150573f7d79099097ad5c5fd8f31ce915d5c88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:21:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029027c6d63baf7bfb9843abd2fc2b739a48610216f6132b6edae462f0e70734`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 5.6 MB (5567166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9545252869703d4ce0e49fcdf41cd588fe96835981a05369a36ce986020e28c`  
		Last Modified: Tue, 18 Nov 2025 16:03:34 GMT  
		Size: 177.4 MB (177412364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7ef2dadcdb140ad4b9f2b3f3829abe44b958b9a512f807804900d532bb7ae924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4843b55b5922d4066c7f8f3b168bbc1d4c2b89f00a994633d065684b1184026c`

```dockerfile
```

-	Layers:
	-	`sha256:8a6ff17a86147fb1fadaa3a71d31e969243eaf0896367426923006db64cd4b02`  
		Last Modified: Tue, 18 Nov 2025 06:04:01 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7d6fa523d4c3f549df4f16cac0945b6acba055e8e734f97d319f98a42faaa8`  
		Last Modified: Tue, 18 Nov 2025 06:04:02 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:326af20227013fbdd0156b2d2ee43db097484c827fcc3aec43fa4925e4ba3ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c921fbab4361fcba7d253fc77de5537d5a542f663815c9fbc9a0f6d983ac364e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:42 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddf024a336add7a4bafd65783505344c840e3b64ef41d5a68fc540092ddc09`  
		Last Modified: Tue, 18 Nov 2025 02:18:16 GMT  
		Size: 5.9 MB (5878045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0974eea60241dff1791390f05414a3817f6bbd4defa337d806a4d83166f5e2`  
		Last Modified: Tue, 18 Nov 2025 02:18:08 GMT  
		Size: 157.8 MB (157807896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88776365c66fe4d3148f220baf334f4b674412fe6da649aa9778403dd7134e2`  
		Last Modified: Tue, 18 Nov 2025 02:18:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8a7b9ce85a0ca059b2b718b53460c232e85f29167b9b464206f4b1945cb68a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267488b28cf6c60e10a924367fa711ebd7d55b57a1e4cd95e1c03f8aa2abd084`

```dockerfile
```

-	Layers:
	-	`sha256:575fbafb05234551dc16bb57a360f4bf010103579ab27ba7c970887ca9757627`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f856465ed88fe4eb461f74180038b639c6293359b5861332e985f739c00a8c9b`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:1bf868a2bbd05fc69edbf1e4373833db83eb5b228b46f21c5ed9a53b10413d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b07b177a9c9eae6c41790122e166f51518ff1955d9a6c2869d4fae4781aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:16:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940cffb1d6213886988c4c3af3f5f6a0cc37446b6878a8e2362ae10674c75ca`  
		Last Modified: Tue, 18 Nov 2025 02:16:58 GMT  
		Size: 155.4 MB (155354870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5ed149e466cf636d1d47da92f0c9f90446f713ada2c3166034e0926e10e9c`  
		Last Modified: Tue, 18 Nov 2025 02:17:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:21a1ab46f506a7f4ed9e147dac642116d38a0cbd6ba7f662e90d9e9d11f3e0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4de383be6b49ff52003f8e52872e47baf8d2cb858fb56d1b68d77ecbd3ff2d5`

```dockerfile
```

-	Layers:
	-	`sha256:741d0c0be3f8b98b8d14a923b3453801cce2a243bc99e86a3ab73a1fac526c89`  
		Last Modified: Tue, 18 Nov 2025 06:04:10 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed32c4698b545c221a8efa988a4627102accb5850943951be72ecba9f68334b7`  
		Last Modified: Tue, 18 Nov 2025 06:04:11 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10-trixie`

```console
$ docker pull julia@sha256:f5e2a878e14dcc5e6c4f63a12e9f994db0539e4c4d3292c1b85eb92c463079ee
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
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
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
$ docker pull julia@sha256:a2b6f5a6a95d9c683292573eccb843e8b54aa433a6ba14303e729f974db13049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d47e5e780c6d6b04f7050bc6c19aa3ae6d993a5bb47b4192bea88d1cfb0dacda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:f48a86cec5e53df7158d643facd17ae90ac31141e7c1316cbd8a68de962e16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.10-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10`

```console
$ docker pull julia@sha256:70ac1a43be2ee61dc22dbb3d51a41ef0dad18be2dc42dcbf6d1e3ee56aa1f5a4
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
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10.10` - linux; amd64

```console
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
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

### `julia:1.10.10` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
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
$ docker pull julia@sha256:5381d01c3615422f73fde38e729f1817068c6b5bab9160ba2d98b243b352217f
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
$ docker pull julia@sha256:299c3c8333df7a50dcd02ebccef345b1f88048f6c7d892001481cd378c5d46cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210269661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c18876753015f55ad8389bc1856f4d5d847bfbadb6b3146d0b023332bbeca92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:22:46 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:22:46 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:22:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:22:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:22:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82be4ab744883e883a44090eab187db08ad07885ee0d0e0a30d296c508fb12ba`  
		Last Modified: Tue, 18 Nov 2025 04:23:25 GMT  
		Size: 5.7 MB (5716399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686df9e4f2726cc605d0bb4489f6b0259b3b543877e935cd58c1183252aa4b21`  
		Last Modified: Tue, 18 Nov 2025 06:11:30 GMT  
		Size: 176.3 MB (176324443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8061c64217926f23766909405893cb28a9640e36e487fbc69b8eb50a226575d2`  
		Last Modified: Tue, 18 Nov 2025 04:23:24 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9174cb7321d5fb61b395fd1388ace0d42af55407c54f50a81b74f66515b9bdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f4d25e0e4acc0b84213fc7c5f7bae960ae76aeac5a4ec60332e591ace7ba26`

```dockerfile
```

-	Layers:
	-	`sha256:18a0814e0c9aa4c785962304e74d9d35451f6f8e418467e8091daa6af258b9c7`  
		Last Modified: Tue, 18 Nov 2025 06:03:57 GMT  
		Size: 2.6 MB (2568318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da5bbba4e084f79beb08d7b46c9429e44212f1262b14763c5f4716f4ae8d715`  
		Last Modified: Tue, 18 Nov 2025 06:03:58 GMT  
		Size: 16.6 KB (16598 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:2f54cb3c7b23e9497c60cacc75eaef83da3df5a0f7fc96e467ad90b141df7acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e0059c86daa089e2f731ea3150573f7d79099097ad5c5fd8f31ce915d5c88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:21:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029027c6d63baf7bfb9843abd2fc2b739a48610216f6132b6edae462f0e70734`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 5.6 MB (5567166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9545252869703d4ce0e49fcdf41cd588fe96835981a05369a36ce986020e28c`  
		Last Modified: Tue, 18 Nov 2025 16:03:34 GMT  
		Size: 177.4 MB (177412364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:7ef2dadcdb140ad4b9f2b3f3829abe44b958b9a512f807804900d532bb7ae924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4843b55b5922d4066c7f8f3b168bbc1d4c2b89f00a994633d065684b1184026c`

```dockerfile
```

-	Layers:
	-	`sha256:8a6ff17a86147fb1fadaa3a71d31e969243eaf0896367426923006db64cd4b02`  
		Last Modified: Tue, 18 Nov 2025 06:04:01 GMT  
		Size: 2.6 MB (2567335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7d6fa523d4c3f549df4f16cac0945b6acba055e8e734f97d319f98a42faaa8`  
		Last Modified: Tue, 18 Nov 2025 06:04:02 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; 386

```console
$ docker pull julia@sha256:326af20227013fbdd0156b2d2ee43db097484c827fcc3aec43fa4925e4ba3ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192896018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c921fbab4361fcba7d253fc77de5537d5a542f663815c9fbc9a0f6d983ac364e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:42 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:42 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ddf024a336add7a4bafd65783505344c840e3b64ef41d5a68fc540092ddc09`  
		Last Modified: Tue, 18 Nov 2025 02:18:16 GMT  
		Size: 5.9 MB (5878045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0974eea60241dff1791390f05414a3817f6bbd4defa337d806a4d83166f5e2`  
		Last Modified: Tue, 18 Nov 2025 02:18:08 GMT  
		Size: 157.8 MB (157807896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88776365c66fe4d3148f220baf334f4b674412fe6da649aa9778403dd7134e2`  
		Last Modified: Tue, 18 Nov 2025 02:18:14 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:8a7b9ce85a0ca059b2b718b53460c232e85f29167b9b464206f4b1945cb68a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2582049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267488b28cf6c60e10a924367fa711ebd7d55b57a1e4cd95e1c03f8aa2abd084`

```dockerfile
```

-	Layers:
	-	`sha256:575fbafb05234551dc16bb57a360f4bf010103579ab27ba7c970887ca9757627`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 2.6 MB (2565475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f856465ed88fe4eb461f74180038b639c6293359b5861332e985f739c00a8c9b`  
		Last Modified: Tue, 18 Nov 2025 06:04:06 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:1bf868a2bbd05fc69edbf1e4373833db83eb5b228b46f21c5ed9a53b10413d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193680362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b07b177a9c9eae6c41790122e166f51518ff1955d9a6c2869d4fae4781aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:02 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:02 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:16:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0940cffb1d6213886988c4c3af3f5f6a0cc37446b6878a8e2362ae10674c75ca`  
		Last Modified: Tue, 18 Nov 2025 02:16:58 GMT  
		Size: 155.4 MB (155354870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e5ed149e466cf636d1d47da92f0c9f90446f713ada2c3166034e0926e10e9c`  
		Last Modified: Tue, 18 Nov 2025 02:17:03 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:21a1ab46f506a7f4ed9e147dac642116d38a0cbd6ba7f662e90d9e9d11f3e0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4de383be6b49ff52003f8e52872e47baf8d2cb858fb56d1b68d77ecbd3ff2d5`

```dockerfile
```

-	Layers:
	-	`sha256:741d0c0be3f8b98b8d14a923b3453801cce2a243bc99e86a3ab73a1fac526c89`  
		Last Modified: Tue, 18 Nov 2025 06:04:10 GMT  
		Size: 2.6 MB (2571600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed32c4698b545c221a8efa988a4627102accb5850943951be72ecba9f68334b7`  
		Last Modified: Tue, 18 Nov 2025 06:04:11 GMT  
		Size: 16.6 KB (16632 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.10.10-trixie`

```console
$ docker pull julia@sha256:f5e2a878e14dcc5e6c4f63a12e9f994db0539e4c4d3292c1b85eb92c463079ee
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
$ docker pull julia@sha256:44e86fb360ef0a232637167abe1baf8505e5761cc91c8ebb504f6fe1acf50eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212382094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7857a283794890a9566a3f31bf96a918f91cf48b8e66659f99298bc5c1b71eaf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:21:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:47 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:47 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 04:21:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:47 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996b8548207b9ba58876d642af5a558c655fa1296acc2eb700f3ee407cc4a9ef`  
		Last Modified: Tue, 18 Nov 2025 04:22:24 GMT  
		Size: 6.2 MB (6242855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5f498520761218d69992d7e5ac7bfa54d9214e143b48bae2b12500fe9f7842`  
		Last Modified: Tue, 18 Nov 2025 06:58:23 GMT  
		Size: 176.4 MB (176362385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf756a4557e12006232aea42b5d75450ce55aafffff7d66c23b3036bbd3bf10`  
		Last Modified: Tue, 18 Nov 2025 04:22:23 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:1bc92809e2a7fa48493bcde5fb5660a7f9458a82f9afbec79e65cb324ae31aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5840d23af02ee75143df204ec213aa70d2be471774fb4aa0706cd80074a4b839`

```dockerfile
```

-	Layers:
	-	`sha256:f47f4e38530390f813cf5f1fc361c241d227a5d7c7b618c37df2662d8a90e7a3`  
		Last Modified: Tue, 18 Nov 2025 06:03:42 GMT  
		Size: 2.2 MB (2240183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d98d4a029809aed2602e196164085c2d99a260518d2ee65cf43b93d0363710`  
		Last Modified: Tue, 18 Nov 2025 06:03:43 GMT  
		Size: 17.2 KB (17168 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:ff08ad78d2efd98947e3c290b7ceb053f10ad643197703ea860d15985bec87c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.7 MB (213742572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8faa3c389c32695dc8a3c02bdea0546f292aa6469907dcc2d901ba05f020bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7476c6bc9fcf378e56b1f826c6f789ef7624026b9a206ad1431a95b62bcb082`  
		Last Modified: Tue, 18 Nov 2025 02:22:09 GMT  
		Size: 6.2 MB (6153421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c0eccae9514a15e67031005ff7fb3059039f8bdb6d6f3c58095bd138f69e73`  
		Last Modified: Tue, 18 Nov 2025 06:42:37 GMT  
		Size: 177.5 MB (177450170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ef85ea11bd1c3cfe76e1b1318d53a85b61a8aa650112599e78c4eade488362`  
		Last Modified: Tue, 18 Nov 2025 02:22:07 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1e32ce348bd649d719e9691318b74984bd2978e2246713ab5bcf85da70b6029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccaeeb70ab51c0ee9f933f9b7e3eff1f91b31461e660fa21136d54dd4376877`

```dockerfile
```

-	Layers:
	-	`sha256:6c909a6d61a9b3dd7193ff4f7d51e0683a2a65ad1deb8ba04f501fbb1dc33068`  
		Last Modified: Tue, 18 Nov 2025 06:03:47 GMT  
		Size: 2.2 MB (2239233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3bf7d89c5742c5090d9904716b20fd9fd51ea308f8d0e4f1f2d774b11cfd5c5`  
		Last Modified: Tue, 18 Nov 2025 06:03:48 GMT  
		Size: 17.3 KB (17287 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.10.10-trixie` - linux; 386

```console
$ docker pull julia@sha256:b47d7fe6fbd1b9caa6ca77ba6dce32be31ffcec1458377e00a5122b5b896b403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195562913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31e2c7d5e7e5630a360204fb891b72d85d53ac1d036550c9a0c61691274e489`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:10 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:10 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 18 Nov 2025 02:17:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.10/julia-1.10.10-linux-x86_64.tar.gz'; 			sha256='6a78a03a71c7ab792e8673dc5cedb918e037f081ceb58b50971dfb7c64c5bf81'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.10/julia-1.10.10-linux-aarch64.tar.gz'; 			sha256='a4b157ed68da10471ea86acc05a0ab61c1a6931ee592a9b236be227d72da50ff'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.10/julia-1.10.10-linux-i686.tar.gz'; 			sha256='32186f38e7f6c7830375da1d1327bec3b187d93e3f0ff007829f20f578fd8c35'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.10/julia-1.10.10-linux-ppc64le.tar.gz'; 			sha256='f47516c511f100670cad72f3c7a1d95d2c20862f1aa14b1162b0b90424167f16'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7837d029b499f335088799d90f7a786e9e3c75d90d0ab7a51465c69dbf79ddb2`  
		Last Modified: Tue, 18 Nov 2025 02:17:42 GMT  
		Size: 6.4 MB (6427653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85287d91ba6d08f0b2725705ad370fb69e858d91986e99e3ded06a91888211de`  
		Last Modified: Tue, 18 Nov 2025 02:17:36 GMT  
		Size: 157.8 MB (157841822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89c93595683f02dec833cca0c94b4865008cd2abfb3abd0119b96cb3d8682b`  
		Last Modified: Tue, 18 Nov 2025 02:17:41 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.10.10-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:78a936b91d804b2372fc0ca3250ccba393da0582c630834172ad56dc6ff02adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb1437cde3897b2497ba5a49767e847c40e0c3926139c73c2741c6dd81b06c`

```dockerfile
```

-	Layers:
	-	`sha256:e58b1e50f16668cf504211d23a09115208b93116c67ba8f72fe8aae6a3fd5a04`  
		Last Modified: Tue, 18 Nov 2025 06:03:51 GMT  
		Size: 2.2 MB (2237328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2816b0a63a2c63a0321053eb17198d6f102a615a900e8989532b120fb2c73d5`  
		Last Modified: Tue, 18 Nov 2025 06:03:52 GMT  
		Size: 17.1 KB (17131 bytes)  
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
$ docker pull julia@sha256:a2b6f5a6a95d9c683292573eccb843e8b54aa433a6ba14303e729f974db13049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10.10-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.10.10-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d47e5e780c6d6b04f7050bc6c19aa3ae6d993a5bb47b4192bea88d1cfb0dacda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.10.10-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:7edb72759b388f38a9b0e46fdd96facd85389d18514a82679d427c952e288b58
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1958890618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630d5290d46f62ec123d6cad7f215024bdfd8cda245bde29b581cf0aeebeb40f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:59 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:12:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:12:01 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:13:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:13:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f19e7acd3eff7b7e6c7ea7774ec664b73f55302d63d7638b2ad2b34f9c37fca`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77eb82c958103ec6141e0a9a599b8bc49c0dbd5d08826e6c366abe729d79682b`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6e6a42c5c415a7a75db0dcd1e542d96b5806c9af8eae68803423b2fad8aceb`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cdcd404cfaa709f66f97bc220ee78acef6dafb93ca0bef1a5cd2c523685060`  
		Last Modified: Tue, 11 Nov 2025 21:03:12 GMT  
		Size: 188.9 MB (188922558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc641b0f5cc67b708ab9c2623be14827f4655edd8a988c72ef85667b983c1ec8`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.10.10-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:f48a86cec5e53df7158d643facd17ae90ac31141e7c1316cbd8a68de962e16a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.10.10-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:9e4b89633dc536d08a037c6617e9d7751036e12acabebf42d07ef88d4ac1a28f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3424271000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cccbb27e32333ac892b369c650eca7f3739b5076488a7b5d52b6fa8438da5af`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:18 GMT
ENV JULIA_VERSION=1.10.10
# Tue, 11 Nov 2025 19:13:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.10-win64.exe
# Tue, 11 Nov 2025 19:13:20 GMT
ENV JULIA_SHA256=c2a9087064a193e8c2219cc03fac2264445bc9ccf626e30acc39ebd5fa7ad09f
# Tue, 11 Nov 2025 19:14:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8285ac56aa8dfc6927624dc14fae2bfc7d25d53da7342eb169af1b4433e08d02`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60efe69b618d1d1d30e54cb9084fcfe1bb7df62307fd2450214bf30bbc577ad5`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184105fbf2dc023cd3c097418fc81b56b1dd4257353d361bd2fb09288e12cffd`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5170a2723591549079334bff4a0d3e5af390adaf11582659aaf3eb449f4f1f44`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632e0489d1e7f94a5ef9ebb57acc6eb73ee8f33eaec19f7494c9d125112a1644`  
		Last Modified: Tue, 11 Nov 2025 21:03:07 GMT  
		Size: 188.8 MB (188808719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888a7990b3c96f1c1a08c1b891c8dfc6cb10901b99a88e844a51a4f817ce108c`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11`

```console
$ docker pull julia@sha256:0752abb483350551715494c774bf2250b1f41fd7c5cb301af020d119c5291437
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
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11` - linux; amd64

```console
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 02:22:20 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Tue, 18 Nov 2025 02:17:44 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
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
		Last Modified: Mon, 10 Nov 2025 04:21:57 GMT  
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

### `julia:1.11` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-bookworm`

```console
$ docker pull julia@sha256:8b0ad8e6d29ed3767dcbc838f778c1f092fd68b9f7f4ff9060ee3fac461c9269
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
$ docker pull julia@sha256:f4d3fac0fa62fb597cc498694fb26973346b837b9d14926dc8d5f6fc17d32c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c242212b04129672d2d70409ef0274ed477a2612e5db3c901967ea10d61ae11e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:21:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64287521fae1ed74e55d6db247c476f376f6326d8692b926ddaff00d264660e`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 5.7 MB (5716403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a695f03af55a8be1b1c5d34345a35e3f2d95d1ae0ce06fd24a16c32d0016110`  
		Last Modified: Tue, 18 Nov 2025 07:26:54 GMT  
		Size: 288.8 MB (288788343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4ab0dafaefcf335596cd20cdb877acd34f9746b8f0b69cc01f3f359b964eff`  
		Last Modified: Tue, 18 Nov 2025 04:22:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:93247f777bb0a6004b5af30109be1404066ebbce81229f9e8ccccb23ac61f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc357a4f5c3b5ecb668442c6af292c7fa41801319ad9ba7489242ce108260aa8`

```dockerfile
```

-	Layers:
	-	`sha256:af0a12fa1bbaf70991bc885de8a505ad526520a0328a2ef2a64769262d6c565e`  
		Last Modified: Tue, 18 Nov 2025 06:04:34 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba641224ecb950287995cc172d09e26d07e19ad4ba0255e4ca5308125df15002`  
		Last Modified: Tue, 18 Nov 2025 06:04:35 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:919245c9db92ef7b659033cc127763743edc8ca281c0e225d0dcb2d9d8e89d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c9d30335a960582fb6e9f651d35c90d160ec47e42868e7f228fa83132cc743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18288eecc7d13e180b657797c35b3effcf06ed2ebd361ab629425ebc62a7bab8`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 5.6 MB (5567234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac828501f908b9f48f5885eadac374ee7f922484e46f80bc0c6ee521c97f0b0d`  
		Last Modified: Tue, 18 Nov 2025 15:58:28 GMT  
		Size: 304.6 MB (304646684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f5a7472d204b48f1950002bbd423e6cb2e6289962ce1c0f3c1df7c1006d92`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c8015ebeb6a0e77e23f0fe91ad9af9de35ffaf91dcdd41871b0a1bacb166391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea88c5abf5f30fca45d2a7daff6e7b1ddfd3003ca722d9c2f4b6e2bd87662896`

```dockerfile
```

-	Layers:
	-	`sha256:9402a4dc9677dff56f41041cd0c3ac6a481b0b58103190677fa95306f90dd1ac`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed27def1e4d1e40761b2b1578c8e2deaf73fc2b96f9e11f28c03f8b70713c993`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; 386

```console
$ docker pull julia@sha256:11d819490d1e0c57b5b061274f9bc61ae318c0562d83efb62fd1015f1bf233ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272644038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bdd32af1842a4d2659f39093f8eccbc1f530f4f70d5fff6be544d0b9449b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:16:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6c2944a3e4a21302a0da032ef214c48cb9f90d1080bb8e7e5a91352da8a25f`  
		Last Modified: Tue, 18 Nov 2025 02:17:53 GMT  
		Size: 5.9 MB (5878013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d24a2d660d447f48321101946c660576d6cc6398982e88eabbe9c775f2694`  
		Last Modified: Tue, 18 Nov 2025 02:17:47 GMT  
		Size: 237.6 MB (237555950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecd266f7fb1d9e83c2f32cb3736bc25ec4774cc0e48c6dbb9e88eec8d96ad17`  
		Last Modified: Tue, 18 Nov 2025 02:17:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:55926a10717573cfefa42d136a7ac2bdfe777eeb02d64d07612991f429e74cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56248d7ceb4cfff8e6de0bde3aa70f0d0135762fa4e1327823e936b97c8fa40a`

```dockerfile
```

-	Layers:
	-	`sha256:2cd6b96b703977047157234643d1afdf22318a7c63e4d196ca867504d9518892`  
		Last Modified: Tue, 18 Nov 2025 06:04:44 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca04cfc1c6b84dff7aa8b2519d6c4a686e4596df58fe1d51abf1f65c92b2181`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 16.6 KB (16559 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:8d082d3a7e7a25545da61230d6fceaa10082c096d21937d1d7a4210121cd645d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b11a2f611440efabfebbd4c757f6df26c32ecbabd07c4c9720a14085623a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:15:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545cbd5cb3ec9f6e7b77c8c205f3530ef980328f28e70238a8f01a961d67006`  
		Last Modified: Tue, 18 Nov 2025 02:16:41 GMT  
		Size: 248.6 MB (248553764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c207300b970e725e6aa586c4daf1df0c17e96424840111b1042e770313f44f1`  
		Last Modified: Tue, 18 Nov 2025 02:16:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:592b7fe5984b3e4b42c2098f9dff3a1c81b5740a594d236f2f1d1b8b93c658d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f603dd87ba3035670e1ce7c406579dea1fdb731285bdaca11664a6de73f1bd46`

```dockerfile
```

-	Layers:
	-	`sha256:0f2987138af0e36f3f5dd87a6ec1be82c8215ee827989b8f809963942aeec870`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ce1020bfaaae1bf087a40ff5243eac648bcaf4ea4c6f325af3ccb2db2a942d`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 16.6 KB (16617 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11-trixie`

```console
$ docker pull julia@sha256:a8d6a77271df35b5bd36c478d082a01d56ffa78b8b937129000b7600ca413f89
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
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 02:22:20 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11-trixie` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Tue, 18 Nov 2025 02:17:44 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
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
		Last Modified: Mon, 10 Nov 2025 04:21:57 GMT  
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
$ docker pull julia@sha256:f39ce3c0c4452cd4b8bb48d6c450406e1a97e489fbdcf604c45108b624a7223a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc92d61aa4d6379ee1a080d7ce3fc363fd49b454b56cc59922b525f5b2dedcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:8c85dee4e7029daaf9fe98159f6df607df9624343b01d932732b01fddc2290ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.11-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7`

```console
$ docker pull julia@sha256:0752abb483350551715494c774bf2250b1f41fd7c5cb301af020d119c5291437
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
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11.7` - linux; amd64

```console
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 02:22:20 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Tue, 18 Nov 2025 02:17:44 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
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
		Last Modified: Mon, 10 Nov 2025 04:21:57 GMT  
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

### `julia:1.11.7` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-bookworm`

```console
$ docker pull julia@sha256:8b0ad8e6d29ed3767dcbc838f778c1f092fd68b9f7f4ff9060ee3fac461c9269
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
$ docker pull julia@sha256:f4d3fac0fa62fb597cc498694fb26973346b837b9d14926dc8d5f6fc17d32c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322733564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c242212b04129672d2d70409ef0274ed477a2612e5db3c901967ea10d61ae11e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:20:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:21:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:21:13 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:21:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:21:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:21:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64287521fae1ed74e55d6db247c476f376f6326d8692b926ddaff00d264660e`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 5.7 MB (5716403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a695f03af55a8be1b1c5d34345a35e3f2d95d1ae0ce06fd24a16c32d0016110`  
		Last Modified: Tue, 18 Nov 2025 07:26:54 GMT  
		Size: 288.8 MB (288788343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4ab0dafaefcf335596cd20cdb877acd34f9746b8f0b69cc01f3f359b964eff`  
		Last Modified: Tue, 18 Nov 2025 04:22:11 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:93247f777bb0a6004b5af30109be1404066ebbce81229f9e8ccccb23ac61f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2583665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc357a4f5c3b5ecb668442c6af292c7fa41801319ad9ba7489242ce108260aa8`

```dockerfile
```

-	Layers:
	-	`sha256:af0a12fa1bbaf70991bc885de8a505ad526520a0328a2ef2a64769262d6c565e`  
		Last Modified: Tue, 18 Nov 2025 06:04:34 GMT  
		Size: 2.6 MB (2567082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba641224ecb950287995cc172d09e26d07e19ad4ba0255e4ca5308125df15002`  
		Last Modified: Tue, 18 Nov 2025 06:04:35 GMT  
		Size: 16.6 KB (16583 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:919245c9db92ef7b659033cc127763743edc8ca281c0e225d0dcb2d9d8e89d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338316497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c9d30335a960582fb6e9f651d35c90d160ec47e42868e7f228fa83132cc743`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:28 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:28 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:28 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18288eecc7d13e180b657797c35b3effcf06ed2ebd361ab629425ebc62a7bab8`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 5.6 MB (5567234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac828501f908b9f48f5885eadac374ee7f922484e46f80bc0c6ee521c97f0b0d`  
		Last Modified: Tue, 18 Nov 2025 15:58:28 GMT  
		Size: 304.6 MB (304646684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9f5a7472d204b48f1950002bbd423e6cb2e6289962ce1c0f3c1df7c1006d92`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 372.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:9c8015ebeb6a0e77e23f0fe91ad9af9de35ffaf91dcdd41871b0a1bacb166391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea88c5abf5f30fca45d2a7daff6e7b1ddfd3003ca722d9c2f4b6e2bd87662896`

```dockerfile
```

-	Layers:
	-	`sha256:9402a4dc9677dff56f41041cd0c3ac6a481b0b58103190677fa95306f90dd1ac`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.6 MB (2567333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed27def1e4d1e40761b2b1578c8e2deaf73fc2b96f9e11f28c03f8b70713c993`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; 386

```console
$ docker pull julia@sha256:11d819490d1e0c57b5b061274f9bc61ae318c0562d83efb62fd1015f1bf233ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272644038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bdd32af1842a4d2659f39093f8eccbc1f530f4f70d5fff6be544d0b9449b5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:16:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:07 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:07 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6c2944a3e4a21302a0da032ef214c48cb9f90d1080bb8e7e5a91352da8a25f`  
		Last Modified: Tue, 18 Nov 2025 02:17:53 GMT  
		Size: 5.9 MB (5878013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d24a2d660d447f48321101946c660576d6cc6398982e88eabbe9c775f2694`  
		Last Modified: Tue, 18 Nov 2025 02:17:47 GMT  
		Size: 237.6 MB (237555950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecd266f7fb1d9e83c2f32cb3736bc25ec4774cc0e48c6dbb9e88eec8d96ad17`  
		Last Modified: Tue, 18 Nov 2025 02:17:52 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:55926a10717573cfefa42d136a7ac2bdfe777eeb02d64d07612991f429e74cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2580798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56248d7ceb4cfff8e6de0bde3aa70f0d0135762fa4e1327823e936b97c8fa40a`

```dockerfile
```

-	Layers:
	-	`sha256:2cd6b96b703977047157234643d1afdf22318a7c63e4d196ca867504d9518892`  
		Last Modified: Tue, 18 Nov 2025 06:04:44 GMT  
		Size: 2.6 MB (2564239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca04cfc1c6b84dff7aa8b2519d6c4a686e4596df58fe1d51abf1f65c92b2181`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 16.6 KB (16559 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-bookworm` - linux; ppc64le

```console
$ docker pull julia@sha256:8d082d3a7e7a25545da61230d6fceaa10082c096d21937d1d7a4210121cd645d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286879258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b11a2f611440efabfebbd4c757f6df26c32ecbabd07c4c9720a14085623a5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:20 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:20 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:15:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbb1328f577fb2b5f0a982d2d5d2be5abaa1e6af9a58529f7782e0c4528dc5a`  
		Last Modified: Tue, 18 Nov 2025 02:16:47 GMT  
		Size: 6.3 MB (6256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545cbd5cb3ec9f6e7b77c8c205f3530ef980328f28e70238a8f01a961d67006`  
		Last Modified: Tue, 18 Nov 2025 02:16:41 GMT  
		Size: 248.6 MB (248553764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c207300b970e725e6aa586c4daf1df0c17e96424840111b1042e770313f44f1`  
		Last Modified: Tue, 18 Nov 2025 02:16:46 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:592b7fe5984b3e4b42c2098f9dff3a1c81b5740a594d236f2f1d1b8b93c658d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2588215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f603dd87ba3035670e1ce7c406579dea1fdb731285bdaca11664a6de73f1bd46`

```dockerfile
```

-	Layers:
	-	`sha256:0f2987138af0e36f3f5dd87a6ec1be82c8215ee827989b8f809963942aeec870`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 2.6 MB (2571598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ce1020bfaaae1bf087a40ff5243eac648bcaf4ea4c6f325af3ccb2db2a942d`  
		Last Modified: Tue, 18 Nov 2025 06:04:49 GMT  
		Size: 16.6 KB (16617 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.11.7-trixie`

```console
$ docker pull julia@sha256:a8d6a77271df35b5bd36c478d082a01d56ffa78b8b937129000b7600ca413f89
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
$ docker pull julia@sha256:070d9543b98eeffbb2167681daa6012ad8ea98be87298a8fee3e681fd6e3bf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.8 MB (324845390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceceb5ca4d279cfc1063d9339d1d42fefb4d931d888488e75759ab3b4e61518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:20:43 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:20:43 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 04:20:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:20:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:20:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31007bb6a059c55b44ee148e6dd1d1e674e858d59c94cdd3a0c948145b29b508`  
		Last Modified: Tue, 18 Nov 2025 06:12:38 GMT  
		Size: 288.8 MB (288825673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3225482bdcf142c4dcdc5ad731c30bb3afd9ec095ae489e8fd948c5da9e427fe`  
		Last Modified: Tue, 18 Nov 2025 04:21:34 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:f4df5f682b83651f856884f9541c891de09180e44006c004abab22d3bae82f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ecaeb1b2ecff8272e21affe54390c80c220084ef1cc4e417b291fc5d2fb80`

```dockerfile
```

-	Layers:
	-	`sha256:b140340bb4a70b4141693ecaec1720da830425acfe7e839f3fb20288dcfca2ea`  
		Last Modified: Tue, 18 Nov 2025 06:04:21 GMT  
		Size: 2.2 MB (2238945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8fa367481dffcb167e3719bee9c9f06aad92414c51d53daacff3132ada2eb5d`  
		Last Modified: Tue, 18 Nov 2025 06:04:22 GMT  
		Size: 17.1 KB (17150 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:4c618efcfa18315da59ca71a58ce308c0d4cef54fe743cb0b2c37aa341b161b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340965238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1929d2c40589d5075053942fecb3658fccf42e5da01d1581e2ca7cbf21b77d01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:26 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:26 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:21:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:26 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059c82e9b1e65f798bc8d3c5e8a51a4d1157c327f1640e879917c299dc8708b6`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 6.2 MB (6153455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c9ee2722185a7b7ac99892c10da148b805195ec69c0e500754b91855f2f106`  
		Last Modified: Tue, 18 Nov 2025 02:22:20 GMT  
		Size: 304.7 MB (304672803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b840df7c31dc78dac70655ed636874fbd150c008e91d65c77b725cd523f45`  
		Last Modified: Tue, 18 Nov 2025 02:22:26 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:a1cebb205293163f6b6339d4092c5bddb476f3b5bd6e9f2424099d108b099f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91785c858a790083b9036d5c33f000610ba693a1a19534afe9d5587813d25e47`

```dockerfile
```

-	Layers:
	-	`sha256:506743ed574455ae6556cb0de97a287704821590ee7272949dcaa634b9b25c41`  
		Last Modified: Tue, 18 Nov 2025 06:04:40 GMT  
		Size: 2.2 MB (2239229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dfd1b7f08abc5d4ad5d5b67aa95c0102a4311c156060df6997d69bb2bf5d630`  
		Last Modified: Tue, 18 Nov 2025 06:04:41 GMT  
		Size: 17.3 KB (17270 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.11.7-trixie` - linux; 386

```console
$ docker pull julia@sha256:0b9e810b272af0f59a5412055dafad3e70d4ffd5c309a587f2057be3b10cee40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275310517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df20149ad264de3a59dded04bad3480dc32f876e6c9a4e7b0489580272cdfc16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:17:04 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:17:04 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 18 Nov 2025 02:17:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.11/julia-1.11.7-linux-x86_64.tar.gz'; 			sha256='aa5924114ecb89fd341e59aa898cd1882b3cb622ca4972582c1518eff5f68c05'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.11/julia-1.11.7-linux-aarch64.tar.gz'; 			sha256='f97f80b35c12bdaf40c26f6c55dbb7617441e49c9e6b842f65e8410a388ca6f4'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.11/julia-1.11.7-linux-i686.tar.gz'; 			sha256='b0697a58805165a767d875130e3a79f38b5aee9e5080ae95afc67548f3956f32'; 			;; 		'ppc64el') 			url='https://julialang-s3.julialang.org/bin/linux/ppc64le/1.11/julia-1.11.7-linux-ppc64le.tar.gz'; 			sha256='68f1e3a7e530e97aabbe79edfcf38d219348ae5d065a19a7aa652ac57a940b85'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:17:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:17:04 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32543d14a5a42fbcb7119875372c870e3eb377fc446f79f26c9357a0eb901986`  
		Last Modified: Tue, 18 Nov 2025 02:17:51 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35714f03060495511653417b6ad4e018d169c3fe074a7531f8f6df3a8c8bcc1`  
		Last Modified: Tue, 18 Nov 2025 02:17:44 GMT  
		Size: 237.6 MB (237589428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94efaf9ea0eafe1f6958c22508b18cade8997aad47f4e933b8d4411b8adb6f9`  
		Last Modified: Tue, 18 Nov 2025 02:17:49 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.11.7-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:9c2c21bc5b824512c42a48bfb72c0ba234782f029ec3e32638ee5c71c7c08ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2253207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eccfba35a9fce620b0fba074c1d524f8ebfc4d549afe49655308d252d084a0`

```dockerfile
```

-	Layers:
	-	`sha256:9009b49852207c4b1e01f60d01de7b5fd8c9181f26fc792bcf6c3f2be45499cf`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
		Size: 2.2 MB (2236090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829cb5e188c7e7bb6d6c2e894bae6da70662eb990b367ec624b0f64089043bfe`  
		Last Modified: Tue, 18 Nov 2025 06:04:45 GMT  
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
		Last Modified: Mon, 10 Nov 2025 04:21:57 GMT  
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
$ docker pull julia@sha256:f39ce3c0c4452cd4b8bb48d6c450406e1a97e489fbdcf604c45108b624a7223a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11.7-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.11.7-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc92d61aa4d6379ee1a080d7ce3fc363fd49b454b56cc59922b525f5b2dedcd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.11.7-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:c12321a18b2640289ad071e624f2bf2ecc253006226b239b2958b227c08ab315
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056096142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c613627dd5d60bf9eee328c021793543203571070d01e705717716a28469aa`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:38 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:11:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:11:41 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:25 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbf22ed660e8ed9e9ed8b1262ae2de5bc79dc20b8c4c19abf4c6a8bd81b6086`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ea54aab8c7ff1fd92d93d5519eb437f1795ee533f756584997753422a29260`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921b5bec2a9acc78b91ae622eeb01774460fb4da399fc9312b0532b95b1d26b7`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3817c2361192a8f0e9fe864db352a5d4018073c30d18b251e4922d9e3a389fc`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca061c0d33a04d70880dfe8474f7fbf319068743fb65fff2088b194cbe64c731`  
		Last Modified: Tue, 11 Nov 2025 21:03:37 GMT  
		Size: 286.1 MB (286128047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1149ff6138443060525bbc87b499932aeed7ecb7cf81a883878b57f68644d62`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.11.7-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:8c85dee4e7029daaf9fe98159f6df607df9624343b01d932732b01fddc2290ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.11.7-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:eebd3f6a0215cf551f70d603f23eec8ccf1cefa27b921162af1d224c6e21aeeb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3521524833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b362c1dff86b2d195e2f944db4c745527b8e476fbfdf69504533303af0a34f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:16 GMT
ENV JULIA_VERSION=1.11.7
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.7-win64.exe
# Tue, 11 Nov 2025 19:13:17 GMT
ENV JULIA_SHA256=55f260b004c17c1d98226f10ce593c8e79c130fcfc75342ad7cbfcf69d48ebdc
# Tue, 11 Nov 2025 19:14:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:14:43 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed0e561886ca49396c1e9e174bcfaf55afe0d4ebc8ef4a19a365a716b94a2fd`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed81c19f81ad07310053d2a46853bf88581eafa7e795426a3a3bcf288120bc0`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea35c8c45c84005c22c04970e31f7a546bb262f2efb7192e59ebcabfd719975`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1698c4d37ba2b0a36b7f568dbc69ffbd72622b1b44240a5d9ab8b722a81a4bc5`  
		Last Modified: Tue, 11 Nov 2025 19:24:31 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b6c6d3796b41b8595dc6c76d173b98d2959e7f23f114cb18c3f36b5a75045`  
		Last Modified: Tue, 11 Nov 2025 21:03:49 GMT  
		Size: 286.1 MB (286062401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127441e5014abfee576374dd1d5d7dcbb976ffda2d0cd82fd0c927e43a0eecb2`  
		Last Modified: Tue, 11 Nov 2025 19:24:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12`

```console
$ docker pull julia@sha256:f1af93b4fcb73cb431b0ff0c1157d90f82e399a3f541fc5afbcd8e4b0778f35a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12` - linux; amd64

```console
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-bookworm`

```console
$ docker pull julia@sha256:a4be0555a49afd63319b87474c2abbc3bb39d189b91c7afcf880856a08ff2f43
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
$ docker pull julia@sha256:718fae8afcc3d82bee2d8e93b98d357fb91ce67143cd0b3db0eb0d30ad701999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e590adf2e6082fa367e7f681243a7ada431693170e3fbc95f98e267556edfc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:19:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:19:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6196f36242058df76aeed9f9be74444179b9361f55a75d95abce3f2073704`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 5.7 MB (5716358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c89fe608b9302afc559f89092749ddd8047d27f98c5ebab051be79706b58e0`  
		Last Modified: Tue, 18 Nov 2025 12:34:34 GMT  
		Size: 289.5 MB (289470935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba290a3255b38cfcf0e40d2b93602d7c0331965e96dada070859689deb832c2`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:07459013e718289defd96141a743741a998efd75d41d75077dcc86771b546c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534910b59c852b8c4cfeafef23e74a4fdf4514bccda123491b950bc4737db3ea`

```dockerfile
```

-	Layers:
	-	`sha256:ca2dbafbd8fd35f3cd8381ea4ac405b5cc3d725c3c325fa92acbf9fb08ce39ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8b8dc4394b9cfe5c43dd5231757832ea00f02c1fb0e2c68ac60e9b2ab00f69`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b52198fa87dc48d6231e6da93b220c6935033da0f857a20b2eb1f9152f6c0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff38f96d75673ca094cad57f9bd0b2a43173335b695ba04b16938979b4c5c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:21:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db58b4bbda4a603f718f99bd5c8e7d3ac963774cf121fc4d9d9ca8db27cf15`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 5.6 MB (5567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3242c924db6e3b513506ae3c10c101cd9fb859a2137367be3d0524546d3a3`  
		Last Modified: Tue, 18 Nov 2025 02:22:16 GMT  
		Size: 310.2 MB (310205363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c28b844f67c27a9f4854bff15183348e5b52fd5368f44ccd04398dc6d4f6f`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:549b77055b0192f55796e3e14f35fbe2d53d8a896c1ce0ef2657d6764f5a3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f920fa3c749e7d7c93d18ccfd01f56422aa2f989199cf61e98d847c7c1cfbe29`

```dockerfile
```

-	Layers:
	-	`sha256:3ca3f69c58a3d7a3bb4b975209b2de965c357469bbddfa2137163c277baa895b`  
		Last Modified: Tue, 18 Nov 2025 06:03:34 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e67e1e652d5f72a09dd04b91ae3e0fb4c37e3ea8c3ee16e99e03a3fd47cf8be`  
		Last Modified: Tue, 18 Nov 2025 06:03:35 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-bookworm` - linux; 386

```console
$ docker pull julia@sha256:71a6b70c3b3b6307e07b49e0f9ff1519bbb62ddd79126a7be07485bf7c14dae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0cfae68c743761541da4c76d24ab04e660427f0a4dc013baf72fd5aa08de0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:15:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2637d647fce9b735bc6ad4f3ef61b077daf59496f8bc5511b70af849249a2`  
		Last Modified: Tue, 18 Nov 2025 02:16:17 GMT  
		Size: 5.9 MB (5878089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3982f26c9084dc73e80d5e7bf8913a086c4dd9a22462ecd4f65de4c9d33dfa5`  
		Last Modified: Tue, 18 Nov 2025 02:16:10 GMT  
		Size: 231.0 MB (231003052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfb666991d4489bbf89a6f45668e810b3c45f39ef4a1464a0c42e4a47756060`  
		Last Modified: Tue, 18 Nov 2025 02:16:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:999d6ffcb86b5e482c6453855c55eb2f9bf0200938fdd2b9b00861b8c0be5fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0a9eb7698dbbbaf62ac2c022f559cc5ffb7ff52b19c9d0ae783b0337802d7`

```dockerfile
```

-	Layers:
	-	`sha256:1c44b469d322786f4c8698d066fcb0f246eb8df23db3663daff8029e6347a6f9`  
		Last Modified: Tue, 18 Nov 2025 06:03:39 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24641a1bf618df92a443bf98472b79166c077d32e94b2077eb51c0c3ef9ee6ee`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-trixie`

```console
$ docker pull julia@sha256:ff69f979004f8191acdfb9168ed8fa53d60b7fd2b6f2154fc24aa1cf196ad1be
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
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12-trixie` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12-windowsservercore`

```console
$ docker pull julia@sha256:9b2cf26780ab0598b31c3d1b8a5163541515aa48c1615e76d6f4f65b5ae98a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:262db25a6585488ac281d30d018524c7a4dfc7a63fd5d0e9182cbb4c0a5579d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:5a6c083eb99ca2fe16b1308c41034455704607d80b32c8f30a8f3348e4a4737a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.12-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1`

```console
$ docker pull julia@sha256:f1af93b4fcb73cb431b0ff0c1157d90f82e399a3f541fc5afbcd8e4b0778f35a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12.1` - linux; amd64

```console
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.1` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-bookworm`

```console
$ docker pull julia@sha256:a4be0555a49afd63319b87474c2abbc3bb39d189b91c7afcf880856a08ff2f43
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
$ docker pull julia@sha256:718fae8afcc3d82bee2d8e93b98d357fb91ce67143cd0b3db0eb0d30ad701999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e590adf2e6082fa367e7f681243a7ada431693170e3fbc95f98e267556edfc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:19:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:19:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6196f36242058df76aeed9f9be74444179b9361f55a75d95abce3f2073704`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 5.7 MB (5716358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c89fe608b9302afc559f89092749ddd8047d27f98c5ebab051be79706b58e0`  
		Last Modified: Tue, 18 Nov 2025 12:34:34 GMT  
		Size: 289.5 MB (289470935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba290a3255b38cfcf0e40d2b93602d7c0331965e96dada070859689deb832c2`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:07459013e718289defd96141a743741a998efd75d41d75077dcc86771b546c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534910b59c852b8c4cfeafef23e74a4fdf4514bccda123491b950bc4737db3ea`

```dockerfile
```

-	Layers:
	-	`sha256:ca2dbafbd8fd35f3cd8381ea4ac405b5cc3d725c3c325fa92acbf9fb08ce39ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8b8dc4394b9cfe5c43dd5231757832ea00f02c1fb0e2c68ac60e9b2ab00f69`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b52198fa87dc48d6231e6da93b220c6935033da0f857a20b2eb1f9152f6c0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff38f96d75673ca094cad57f9bd0b2a43173335b695ba04b16938979b4c5c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:21:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db58b4bbda4a603f718f99bd5c8e7d3ac963774cf121fc4d9d9ca8db27cf15`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 5.6 MB (5567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3242c924db6e3b513506ae3c10c101cd9fb859a2137367be3d0524546d3a3`  
		Last Modified: Tue, 18 Nov 2025 02:22:16 GMT  
		Size: 310.2 MB (310205363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c28b844f67c27a9f4854bff15183348e5b52fd5368f44ccd04398dc6d4f6f`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:549b77055b0192f55796e3e14f35fbe2d53d8a896c1ce0ef2657d6764f5a3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f920fa3c749e7d7c93d18ccfd01f56422aa2f989199cf61e98d847c7c1cfbe29`

```dockerfile
```

-	Layers:
	-	`sha256:3ca3f69c58a3d7a3bb4b975209b2de965c357469bbddfa2137163c277baa895b`  
		Last Modified: Tue, 18 Nov 2025 06:03:34 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e67e1e652d5f72a09dd04b91ae3e0fb4c37e3ea8c3ee16e99e03a3fd47cf8be`  
		Last Modified: Tue, 18 Nov 2025 06:03:35 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-bookworm` - linux; 386

```console
$ docker pull julia@sha256:71a6b70c3b3b6307e07b49e0f9ff1519bbb62ddd79126a7be07485bf7c14dae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0cfae68c743761541da4c76d24ab04e660427f0a4dc013baf72fd5aa08de0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:15:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2637d647fce9b735bc6ad4f3ef61b077daf59496f8bc5511b70af849249a2`  
		Last Modified: Tue, 18 Nov 2025 02:16:17 GMT  
		Size: 5.9 MB (5878089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3982f26c9084dc73e80d5e7bf8913a086c4dd9a22462ecd4f65de4c9d33dfa5`  
		Last Modified: Tue, 18 Nov 2025 02:16:10 GMT  
		Size: 231.0 MB (231003052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfb666991d4489bbf89a6f45668e810b3c45f39ef4a1464a0c42e4a47756060`  
		Last Modified: Tue, 18 Nov 2025 02:16:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:999d6ffcb86b5e482c6453855c55eb2f9bf0200938fdd2b9b00861b8c0be5fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0a9eb7698dbbbaf62ac2c022f559cc5ffb7ff52b19c9d0ae783b0337802d7`

```dockerfile
```

-	Layers:
	-	`sha256:1c44b469d322786f4c8698d066fcb0f246eb8df23db3663daff8029e6347a6f9`  
		Last Modified: Tue, 18 Nov 2025 06:03:39 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24641a1bf618df92a443bf98472b79166c077d32e94b2077eb51c0c3ef9ee6ee`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.1-trixie`

```console
$ docker pull julia@sha256:ff69f979004f8191acdfb9168ed8fa53d60b7fd2b6f2154fc24aa1cf196ad1be
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
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:1.12.1-trixie` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:1.12.1-trixie` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:1.12.1-windowsservercore`

```console
$ docker pull julia@sha256:9b2cf26780ab0598b31c3d1b8a5163541515aa48c1615e76d6f4f65b5ae98a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12.1-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1.12.1-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:262db25a6585488ac281d30d018524c7a4dfc7a63fd5d0e9182cbb4c0a5579d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:1.12.1-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:1.12.1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:5a6c083eb99ca2fe16b1308c41034455704607d80b32c8f30a8f3348e4a4737a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:1.12.1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:bookworm`

```console
$ docker pull julia@sha256:a4be0555a49afd63319b87474c2abbc3bb39d189b91c7afcf880856a08ff2f43
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
$ docker pull julia@sha256:718fae8afcc3d82bee2d8e93b98d357fb91ce67143cd0b3db0eb0d30ad701999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323416113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e590adf2e6082fa367e7f681243a7ada431693170e3fbc95f98e267556edfc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 04:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:19:13 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:19:13 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:19:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:19:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:19:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb6196f36242058df76aeed9f9be74444179b9361f55a75d95abce3f2073704`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 5.7 MB (5716358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c89fe608b9302afc559f89092749ddd8047d27f98c5ebab051be79706b58e0`  
		Last Modified: Tue, 18 Nov 2025 12:34:34 GMT  
		Size: 289.5 MB (289470935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba290a3255b38cfcf0e40d2b93602d7c0331965e96dada070859689deb832c2`  
		Last Modified: Tue, 18 Nov 2025 04:20:09 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:07459013e718289defd96141a743741a998efd75d41d75077dcc86771b546c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534910b59c852b8c4cfeafef23e74a4fdf4514bccda123491b950bc4737db3ea`

```dockerfile
```

-	Layers:
	-	`sha256:ca2dbafbd8fd35f3cd8381ea4ac405b5cc3d725c3c325fa92acbf9fb08ce39ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 2.6 MB (2567686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a8b8dc4394b9cfe5c43dd5231757832ea00f02c1fb0e2c68ac60e9b2ab00f69`  
		Last Modified: Tue, 18 Nov 2025 06:03:30 GMT  
		Size: 16.5 KB (16541 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:b52198fa87dc48d6231e6da93b220c6935033da0f857a20b2eb1f9152f6c0703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343875148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff38f96d75673ca094cad57f9bd0b2a43173335b695ba04b16938979b4c5c01`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:21:22 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:21:22 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:21:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:21:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:21:22 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7db58b4bbda4a603f718f99bd5c8e7d3ac963774cf121fc4d9d9ca8db27cf15`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 5.6 MB (5567209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f3242c924db6e3b513506ae3c10c101cd9fb859a2137367be3d0524546d3a3`  
		Last Modified: Tue, 18 Nov 2025 02:22:16 GMT  
		Size: 310.2 MB (310205363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09c28b844f67c27a9f4854bff15183348e5b52fd5368f44ccd04398dc6d4f6f`  
		Last Modified: Tue, 18 Nov 2025 02:22:22 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:549b77055b0192f55796e3e14f35fbe2d53d8a896c1ce0ef2657d6764f5a3cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2584621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f920fa3c749e7d7c93d18ccfd01f56422aa2f989199cf61e98d847c7c1cfbe29`

```dockerfile
```

-	Layers:
	-	`sha256:3ca3f69c58a3d7a3bb4b975209b2de965c357469bbddfa2137163c277baa895b`  
		Last Modified: Tue, 18 Nov 2025 06:03:34 GMT  
		Size: 2.6 MB (2567961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e67e1e652d5f72a09dd04b91ae3e0fb4c37e3ea8c3ee16e99e03a3fd47cf8be`  
		Last Modified: Tue, 18 Nov 2025 06:03:35 GMT  
		Size: 16.7 KB (16660 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:bookworm` - linux; 386

```console
$ docker pull julia@sha256:71a6b70c3b3b6307e07b49e0f9ff1519bbb62ddd79126a7be07485bf7c14dae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266091216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec0cfae68c743761541da4c76d24ab04e660427f0a4dc013baf72fd5aa08de0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:15:31 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:15:31 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:15:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:15:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:15:31 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1fec683ccaf0cadb2cbeb7e9c391ed98964459b2aef26a05e33382cfb2bbdf87`  
		Last Modified: Tue, 18 Nov 2025 01:13:59 GMT  
		Size: 29.2 MB (29209704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be2637d647fce9b735bc6ad4f3ef61b077daf59496f8bc5511b70af849249a2`  
		Last Modified: Tue, 18 Nov 2025 02:16:17 GMT  
		Size: 5.9 MB (5878089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3982f26c9084dc73e80d5e7bf8913a086c4dd9a22462ecd4f65de4c9d33dfa5`  
		Last Modified: Tue, 18 Nov 2025 02:16:10 GMT  
		Size: 231.0 MB (231003052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfb666991d4489bbf89a6f45668e810b3c45f39ef4a1464a0c42e4a47756060`  
		Last Modified: Tue, 18 Nov 2025 02:16:16 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:bookworm` - unknown; unknown

```console
$ docker pull julia@sha256:999d6ffcb86b5e482c6453855c55eb2f9bf0200938fdd2b9b00861b8c0be5fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2581340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa0a9eb7698dbbbaf62ac2c022f559cc5ffb7ff52b19c9d0ae783b0337802d7`

```dockerfile
```

-	Layers:
	-	`sha256:1c44b469d322786f4c8698d066fcb0f246eb8df23db3663daff8029e6347a6f9`  
		Last Modified: Tue, 18 Nov 2025 06:03:39 GMT  
		Size: 2.6 MB (2564833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24641a1bf618df92a443bf98472b79166c077d32e94b2077eb51c0c3ef9ee6ee`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 16.5 KB (16507 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:latest`

```console
$ docker pull julia@sha256:f1af93b4fcb73cb431b0ff0c1157d90f82e399a3f541fc5afbcd8e4b0778f35a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:latest` - linux; amd64

```console
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:latest` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:latest` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:latest` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:trixie`

```console
$ docker pull julia@sha256:ff69f979004f8191acdfb9168ed8fa53d60b7fd2b6f2154fc24aa1cf196ad1be
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
$ docker pull julia@sha256:7f929a3d6d2baa003e6e207ab06cae193565cd896835ca590c3ede0822071274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325529517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0712aa297b917dff43d4662421c87046851e4089c0b4c75a517b4940f56a85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 04:18:23 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 04:18:23 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 04:18:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 04:18:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 04:18:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed699ce64a189bbf9c313dc771f9983ee8f7996f87435d5eaf655d152d541c0a`  
		Last Modified: Tue, 18 Nov 2025 04:19:16 GMT  
		Size: 6.2 MB (6242862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64dde6c93008a6b9c02b80b6cee2653b567d8566b011c7bf27b785bb3b80f87e`  
		Last Modified: Tue, 18 Nov 2025 06:12:12 GMT  
		Size: 289.5 MB (289509803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe5b6315ec128d5f12b078f485bf1cf20da0ab3b19b1b5a798b78c93277595c`  
		Last Modified: Tue, 18 Nov 2025 04:19:15 GMT  
		Size: 368.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:dd7ccbdd853720eea822445d51f66f0f8b6ccfd48ba60d52b42c76fd42c564dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0653c181e7405c47d9c4496443fa1401f25fb90c29ca6a11586b36ced10fe1c4`

```dockerfile
```

-	Layers:
	-	`sha256:af86ad735dea05491bc67320fcf216213ed37b1c83833d110765c9141cab7ca8`  
		Last Modified: Tue, 18 Nov 2025 06:03:19 GMT  
		Size: 2.2 MB (2240123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ed7481c264eb996d4fdeb9e4b27514d5ed26dcd3f273a21689d4d65bd99921`  
		Last Modified: Tue, 18 Nov 2025 06:03:20 GMT  
		Size: 17.7 KB (17683 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; arm64 variant v8

```console
$ docker pull julia@sha256:9b0cbb59e1da02ead8963a5f74727308e07c9ff7fed7b5092cc56da544b78f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.5 MB (346536059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2199e3fa426de2ebaecdfae365e496ddbace69e0ea0ce351038cea71d6efa1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:20:03 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:20:03 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:20:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:20:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d770beafec336b3bce25cfc4997ac8d2fb2e3d55a2a7e5ed0227f1f8122d0f1`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 6.2 MB (6153422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b46134b6cc3d1b99f9157d76088efa7013f51750c73ed5886c836e2972f43f`  
		Last Modified: Tue, 18 Nov 2025 08:00:41 GMT  
		Size: 310.2 MB (310243656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f3990529514d4f54254b5420643f42257feb75a0f9e72371734f352a815abe`  
		Last Modified: Tue, 18 Nov 2025 02:21:02 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:2d52855195dfb1b604e4780c8caabea65044142015bbc3e73739f8343a0eb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2258303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ea94852ee529ed2c36a6bed3ef612043cbfe19dca6fed6dee861f9ab9e6672`

```dockerfile
```

-	Layers:
	-	`sha256:c8d063ff24174b33e03b94210a32f7137316b27b22176bbd56984701713fefac`  
		Last Modified: Tue, 18 Nov 2025 06:03:24 GMT  
		Size: 2.2 MB (2240455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e911a253a6c37d072b13be188549a5956e83a0ed887ce7cb57505fbfc2ad9185`  
		Last Modified: Tue, 18 Nov 2025 06:03:25 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `julia:trixie` - linux; 386

```console
$ docker pull julia@sha256:be6a690b3aa334a2e0fca7123a649100d71182e210b90a574b322c4124b2e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268755298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035df5fd1b528ed3371ce56becdbd8df937449303fdf1f40aecc012971a8ce37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["julia"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_PATH=/usr/local/julia
# Tue, 18 Nov 2025 02:16:50 GMT
ENV PATH=/usr/local/julia/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_GPG=3673DF529D9049477F76B37566E3C7DC03D6E495
# Tue, 18 Nov 2025 02:16:50 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 18 Nov 2025 02:16:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		gnupg 	; 	rm -rf /var/lib/apt/lists/*; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			url='https://julialang-s3.julialang.org/bin/linux/x64/1.12/julia-1.12.1-linux-x86_64.tar.gz'; 			sha256='7d2add9ee74ee2f12b5c268bc194794cc52ea440f8687fbab29db6afefbf69b7'; 			;; 		'arm64') 			url='https://julialang-s3.julialang.org/bin/linux/aarch64/1.12/julia-1.12.1-linux-aarch64.tar.gz'; 			sha256='2e3d6ca07e251721fa3e0cd3460fc240e60f2a9bd97bae0ea2144f586da19297'; 			;; 		'i386') 			url='https://julialang-s3.julialang.org/bin/linux/x86/1.12/julia-1.12.1-linux-i686.tar.gz'; 			sha256='99596fe3f139f52042cb5167034d26823f802dfe3d1333127e504109c03f0807'; 			;; 		*) 			echo >&2 "error: current architecture ($arch) does not have a corresponding Julia binary release"; 			exit 1; 			;; 	esac; 		curl -fL -o julia.tar.gz.asc "$url.asc"; 	curl -fL -o julia.tar.gz "$url"; 		echo "$sha256 *julia.tar.gz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$JULIA_GPG"; 	gpg --batch --verify julia.tar.gz.asc julia.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" julia.tar.gz.asc; 		mkdir "$JULIA_PATH"; 	tar -xzf julia.tar.gz -C "$JULIA_PATH" --strip-components 1; 	rm julia.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		julia --version # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcfa747a3576033e5fae10f2578bb66f9acada3d68a943cbedaedbce07a345a`  
		Last Modified: Tue, 18 Nov 2025 02:17:33 GMT  
		Size: 6.4 MB (6427648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cbd488ed9635dd79e0378c52e17d322fba325b70137dfade6447653eb92341`  
		Last Modified: Tue, 18 Nov 2025 09:58:32 GMT  
		Size: 231.0 MB (231034211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35339b1a319b7a4f8131456dfc140c9a649564e07a4d51cbe6568172f7e51055`  
		Last Modified: Tue, 18 Nov 2025 02:17:32 GMT  
		Size: 371.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `julia:trixie` - unknown; unknown

```console
$ docker pull julia@sha256:c703d8c376caaa985829712234d8e76d9761a35d8c3a49710041a9418b26a95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15ea178e363a63fce1a73cb0c217e3be344685fb8edb7570e6201dc0017c31c`

```dockerfile
```

-	Layers:
	-	`sha256:45aa2e03f9dadf116ab04dc766eb516d8991f4a8a61798b46a7aaf4262d878b3`  
		Last Modified: Tue, 18 Nov 2025 06:03:28 GMT  
		Size: 2.2 MB (2237248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0431b1d1fb59fb247feec5b458737aed9e9ae09ea774f56ceea9c33315c7aa4`  
		Last Modified: Tue, 18 Nov 2025 06:03:29 GMT  
		Size: 17.6 KB (17628 bytes)  
		MIME: application/vnd.in-toto+json

## `julia:windowsservercore`

```console
$ docker pull julia@sha256:9b2cf26780ab0598b31c3d1b8a5163541515aa48c1615e76d6f4f65b5ae98a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `julia:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:262db25a6585488ac281d30d018524c7a4dfc7a63fd5d0e9182cbb4c0a5579d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull julia@sha256:e7a9e0e7f2228fdf2aebdd4f6ce1491138204a8627c5f7f32971f2e7f94470de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2154842910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e0de0f029690af9d9eb47e283d792a14e58702b12622279cd0df8b8ebcfdc7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:11:15 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:11:16 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:11:17 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d4ab77b37e5dc19ae0ddc3cade541563449b175ee5d54a08f19b95597429fe`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527a1293fd21f16021e48ece69fc560b3bd355e7d65ebb9086e89df94c3bfb4e`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4984e7448db863487eddaaaa0923138b75d7aec107e9760246544d10162375d`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3adc6be7472bb055cbc1f35716ed588b8f8d77f366116868833c64907be734`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ba1b12697c1cf6cbd084ed41bce2eb2cb81c3c65dcd5fabd6d159fde007903`  
		Last Modified: Tue, 11 Nov 2025 21:02:58 GMT  
		Size: 384.9 MB (384874906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dfc27729f78c025d371b97ac584330f388a3febfe7c9be3e7362a3dc5b20db4`  
		Last Modified: Tue, 11 Nov 2025 19:22:16 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:5a6c083eb99ca2fe16b1308c41034455704607d80b32c8f30a8f3348e4a4737a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull julia@sha256:a3e9176860eaad2e4f213a5be5e8051a76a63c64e6f8250fb172a66986469f32
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3620238976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1edb18c0d2ebf775fdf2999bd7d17473146464a0ace68a1d54ce7c47d000ef`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:13:30 GMT
ENV JULIA_VERSION=1.12.1
# Tue, 11 Nov 2025 19:13:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Tue, 11 Nov 2025 19:13:32 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Tue, 11 Nov 2025 19:15:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:15:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce403bff4529c458e74fdd64422b24ad14e1175338fcf0a274da91c7f87094a5`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ddadc2ae01dbb69604a5e6df638e1dc0686ebb05acd2311fe63e49f829dc8c6`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f014233672ae8eeef8d45a0911d124f380537241906faa6f8558534322c190`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59735ae4f8b6a6a2933ca03b889e95b97f7b732d4d8a02afc29db56de091b4f2`  
		Last Modified: Tue, 11 Nov 2025 19:24:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155dd7bf0d35967d97fb506a0c601f11783e74c832cc13907d57e01d838ec873`  
		Last Modified: Tue, 11 Nov 2025 21:03:02 GMT  
		Size: 384.8 MB (384776652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82da6199df10340e3c86d1372544522cad75c94b39c6c2a20b6cc72235ce052c`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
